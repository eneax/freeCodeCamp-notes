# Avoid Colorblindness Issues by Using Sufficient Contrast

Color is a large part of visual design, but its use introduces two accessibility issues:

1. color alone should not be used as the only way to convey important information because screen reader users won't see it
2. foreground and background colors need sufficient contrast so colorblind users can distinguish them.

Previous challenges covered having text alternatives to address the first issue. The last challenge introduced contrast checking tools to help with the second. The **WCAG**-recommended contrast ratio of `4.5:1` applies for color use as well as gray-scale combinations.

Colorblind users have trouble distinguishing some colors from others - usually in hue but sometimes lightness as well. You may recall the contrast ratio is calculated using the relative luminance (or lightness) values of the foreground and background colors.

In practice, the 4.5:1 contrast ratio can be reached by shading (adding black to) the darker color and tinting (adding white to) the lighter color. Darker shades on the color wheel are considered to be shades of blues, violets, magentas, and reds, whereas lighter tinted colors are oranges, yellows, greens, and blue-greens.

Example:

```html
<head>
  <style>
    body {
      /* 2.5:1 contrast ratio (NOT GOOD)
      color: hsl(0, 55%, 20%);
      background-color: hsl(120, 25%, 35%); 
      */
      /* 5.9:1 contrast ratio (GOOD) */
      color: hsl(0, 55%, 15%);
      background-color: hsl(120, 25%, 55%);
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
