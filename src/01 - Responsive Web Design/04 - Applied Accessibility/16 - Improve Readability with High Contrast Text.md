# Improve Readability with High Contrast Text

Low contrast between the foreground and background colors can make text difficult to read. Sufficient contrast improves the readability of your content, but what exactly does "sufficient" mean?

The Web Content Accessibility Guidelines (**WCAG**) recommend at least a `4.5` to `1` **contrast ratio** for normal text. The ratio is calculated by comparing the relative luminance values of two colors. This ranges from `1:1` for the same color, or no contrast, to `21:1` for white against black, the strongest contrast.

```html
<head>
  <style>
    body {
      /* color: #d3d3d3; --> 1.5:1 contrast ratio (NOT GOOD) */
      color: #636363; /* 6:1 contrast ratio (GOOD) */
      background-color: #fff;
    }
  </style>
</head>
<body>
  <header>
    <h1>Deep Thoughts with Master Camper Cat</h1>
  </header>
  <article>
    <h2>A Word on the Recent Catnip Doping Scandal</h2>
    <p>
      The influence that catnip has on feline behavior is well-documented, and
      its use as an herbal supplement in competitive ninja circles remains
      controversial. Once again, the debate to ban the substance is brought to
      the public's attention after the high-profile win of Kittytron, a
      long-time proponent and user of the green stuff, at the Claw of Fury
      tournament.
    </p>
    <p>
      As I've stated in the past, I firmly believe a true ninja's skills must
      come from within, with no external influences. My own catnip use shall
      continue as purely recreational.
    </p>
  </article>
</body>
```

**Note**: There are many contrast checking tools available online that calculate this ratio for you.
