Today we're exploring how to control text positioning and appearance with 4 CSS properties: text-align, letter-spacing, word-spacing, and text-transform.
1. text-align — Horizontal Positioning
Controls where text sits inside its container.
css
.left {
  text-align: left;      /* default — text starts at left edge */
}

.center {
  text-align: center;    /* text is centered */
}

.right {
  text-align: right;     /* text hugs the right edge */
}

.justify {
  text-align: justify;   /* text spreads to fill the full width */
}
Important: text-align only works on block-level elements (like <p>, <div>, <h1>). It does not work on inline elements like <span> unless you change their display.
When to use justify: Good for newspaper-style columns. Bad for short lines — it creates awkward gaps between words.

2. letter-spacing — Space Between Letters
Adjusts the gap between individual characters. Use em (relative to font size) or px.
css
/* Tight — letters squeeze together */
.tight-letters {
  letter-spacing: -0.05em;
}

/* Normal — default, no extra space */
.normal-letters {
  letter-spacing: 0;
}

/* Loose — letters spread apart */
.loose-letters {
  letter-spacing: 0.15em;
}

/* Extra loose — dramatic effect, good for headings */
.wide-letters {
  letter-spacing: 0.3em;
  text-transform: uppercase; /* often paired with this */
}
Best practice: Use em instead of px so spacing scales with the font size. Negative values are allowed but be careful — too tight becomes unreadable.

word-spacing — Space Between Words
Similar to letter-spacing, but affects the gaps between whole words instead of characters.
css
/* Default — browser decides */
.normal-words {
  word-spacing: normal;
}

/* Tight words */
.tight-words {
  word-spacing: -2px;
}

/* Loose words */
.loose-words {
  word-spacing: 8px;
}
Real-world use: word-spacing is rarely used for body text. It's more common in creative headings, poetry layouts, or when text-align: justify creates uneven gaps that you want to fine-tune.
4. text-transform — Change Letter Case
Transforms text visually without changing the actual HTML content.
css
/* All lowercase */
.lowercase {
  text-transform: lowercase;   /* "HELLO" becomes "hello" */
}

/* All uppercase */
.uppercase {
  text-transform: uppercase;   /* "hello" becomes "HELLO" */
}

/* First letter of each word capitalized */
.capitalize {
  text-transform: capitalize;  /* "hello world" becomes "Hello World" */
}

/* No transformation */
.none {
  text-transform: none;        /* keeps text exactly as written */
}
Why use this? You might receive data in all-caps from a database, but want to display it nicely. Or you want navigation links in uppercase for style, but keep the HTML readable. It's a presentation layer fix — no need to retype content.
Bonus: Combining Properties
These 4 properties work beautifully together. A common pattern for stylish headings:
css
.stylish-heading {
  text-align: center;
  text-transform: uppercase;
  letter-spacing: 0.2em;
  word-spacing: 0.3em;
  font-weight: 700;
}