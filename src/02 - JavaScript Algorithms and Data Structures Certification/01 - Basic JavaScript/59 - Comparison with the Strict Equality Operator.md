# Comparison with the Strict Equality Operator

While the equality operator (`==`) converts both values that we want to compare to a common type, the strict equality operator (`===`) does not perform a type conversion.

Example:

```js
17 === 17; // true
17 === "17"; // false
```

In the second example, `17` is a `Number` type and `'17'` is a String type; so the strict equality operator considers them unequal.

## From ui.dev

JS Tip: == vs ===

When writing software, the simpler solution is almost always the better one. If in order to use a feature I first have to learn and remember a list of rules pertaining to it, I try my best to avoid it. Not because that feature might not be valuable to know, but because I don’t trust myself to remember every nuanced rule. That logic is the primary decision to why I always use triple equals (===) over double equals (==). They both accomplish similar things, but the Pit of Success for triple equals is much larger, let’s see why.

### Identity Operator (triple equals, ===)

When using triple equals ===, there are two rules you need to remember - strict equality (for when you’re comparing primitive values) and reference equality (for when you’re comparing reference values).

### Strict Equality

Strict equality checks that both the type (number, string, boolean, etc) and the value are the same. If the type is the same but not the value, you’ll get false. If the value is the same but not the type, you’ll get false. If both the value and the type are the same, you’ll get true.

```js
5 === 5; // true. Same type, same value.
5 === 4; // false. Same type, different values.
5 === "5"; // false. Different type, same value.

true === true; // true. Same type, same value.
true === false; // false. Same type, different values.
true === "true"; // false. Different type, same value.
```

Seems simple enough, but as mentioned earlier this rule breaks down when we start to compare reference values (or values that aren’t primitives).

### Reference Equality

As we saw in the previous example, primitives are compared by their value. However, if you use triple equals with reference values, it’s going to compare the references (or spots in memory).

```js
{} === {} // false. Same type, similar value, different reference. ❌
[] === [] // false. Same type, similar value, different reference. ❌
{ name: 'Meg' } === { name: 'Meg' } // false. Same type, similar value, different reference. ❌
```

Even though each of the examples above has the same type and what appears to be the same value, because they’re reference values, JavaScript compares the references in memory, not the actual value. In each of the examples the references or locations in memory are different, which is why we always get false.

We can see this further by assigning two variable to the same reference in memory and then using the identity operator on them.

```js
const user = {
  name: "Tyler"
};

const person = user;

person === user; // true. Same type, same value, same reference.
```

In the example both person and user are referencing the same spot in memory, which is why we get true.

In summary, when using the Identity Operator (===), assuming you know about reference equality, everything just works as you’d expect. Here’s an equality table to prove it.

[equality](https://dorey.github.io/JavaScript-Equality-Table/?ck_subscriber_id=196487204)

### Equality Operator (double equals, ==)

Unlike the Identity Operator (===), unless you’re very familiar with it, odds are the Equality Operator (==) doesn’t behave as you’d expect. Here are just some examples,

```js
"1" == 1; // true
null == undefined; // true
0 == ""; // true
("0" == false[1]) == // true
  true; // true 🤷‍♂️
```

So what exactly is going on here? Notice that each comparison is being made between different types. As we saw earlier with the Identity Operator (===), all of these would return false since they’re all of different types. With the Equality Operator (==), it’s not that simple. Instead of returning false when the types don’t match, it’ll attempt to convert them into the same type.

So in the first example, "1" == 1 because the JavaScript engine will convert the String “1” to Number 1 which then evaluates to 1 == 1 which is true.

It’s that type coercion stage which makes the Equality Operator (==) so unpredictable. Here’s the same equality table we saw before except now in terms of ==.

[equality-2](https://dorey.github.io/JavaScript-Equality-Table/?ck_subscriber_id=196487204)

If you and anyone who works on your codebase is confident in all of JavaScript’s type coercion rules, feel free to use whichever operator you’d like. However, if you’re like me and you’d rather use the tool that works how you’d expect, stick with the Identity Operator (===).
