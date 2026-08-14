Concepts
Project 13 introduces 4 new properties: font-family, font-size, font-weight, and line-height.

1. font-family — Choosing the Font
This sets the typeface. Always provide a fallback stack (comma-separated list) so if the first font isn't available, the browser tries the next one.
css
/* Generic families: serif, sans-serif, monospace, cursive, fantasy */
body {
  font-family: Arial, Helvetica, sans-serif;
}

/* Using a Google Font (you'll link it in HTML <head>) */
h1 {
  font-family: 'Playfair Display', Georgia, serif;
}

/* Monospace for code */
code {
  font-family: 'Courier New', Courier, monospace;
}
Key rule: End your stack with a generic family name (serif, sans-serif, or monospace) so the browser always has something to use.

2. font-size — How Big the Text Is
You can use pixels (px), but rem is preferred for accessibility (it scales with user browser settings).
css
/* Absolute unit — fixed size */
p {
  font-size: 16px;
}

/* Relative unit — scales with root font-size (default is 16px) */
h1 {
  font-size: 2.5rem;   /* 40px if root is 16px */
}

h2 {
  font-size: 1.5rem;   /* 24px */
}

.small-text {
  font-size: 0.875rem; /* 14px */
}
Pro tip: Set html { font-size: 16px; } (or 62.5% for easy math), then use rem everywhere else. This lets users zoom properly.
3. font-weight — How Bold the Text Is
Use named values or numeric values (100–900).
css
/* Named values */
.light {
  font-weight: 300;   /* light */
}

.normal {
  font-weight: 400;   /* normal (default for body text) */
}

.bold {
  font-weight: 700;   /* bold */
}

.extra-bold {
  font-weight: 900;   /* black/heavy */
}
Note: The font you're using must have that weight available. If you ask for font-weight: 100 but only loaded the regular (400) and bold (700) versions, the browser will approximate it.

4. line-height — Vertical Spacing Between Lines
This controls readability. No unit = multiplier of the font size. A value of 1.5 to 1.7 is ideal for body text.
css
/* Bad: tight, hard to read */
.tight {
  line-height: 1.1;
}

/* Good: comfortable reading */
body {
  line-height: 1.6;
}

/* Extra breathing room for headings */
h1 {
  line-height: 1.2;
}

/* You can also use unitless, px, or rem */
.loose {
  line-height: 2;        /* 2x the font size */
}
Best practice: Use unitless numbers (like 1.6 instead of 1.6rem) for line-height. It inherits properly — child elements multiply by their own font size, not the parent's.
Bonus: Google Fonts
For this project, you'll likely want to use fonts beyond the system defaults. Here's how to load Google Fonts in your HTML:
HTML
<!-- In your <head>, BEFORE your CSS link -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;700&family=Playfair+Display:wght@400;700&display=swap" rel="stylesheet">
Then use them in CSS:
css
body { font-family: 'Inter', sans-serif; }
h1 { font-family: 'Playfair Display', serif; }