1. Concepts: Color in CSS
CSS gives you four ways to define a color. Think of them as different languages that all say the same thing.
A. Named Colors (The Easy Way)
CSS knows 140+ color names by heart.
css
.box-red {
  background-color: red;
  color: white;
}
Pros: Human-readable, quick to type
Cons: Limited palette, imprecise
Examples: red, blue, green, tomato, cornflowerblue, mediumseagreen
B. Hexadecimal / Hex (The Web Standard)
Six digits representing Red, Green, Blue. Each pair goes from 00 (none) to FF (full).
css
.box-red {
  background-color: #FF0000;  /* Full red, no green, no blue */
  color: #FFFFFF;             /* White */
  <!-- #00FF00;  green -->
       <!-- #0000ff blue -->
       <!-- #000000 black -->
}
Shorthand: If pairs match, you can use 3 digits.
#FF0000 → #F00
#00FF00 → #0F0
#112233 → #123
Alpha (transparency) with 8-digit hex:
#FF000080 = red at 50% opacity
Pros: Compact, industry standard, millions of colors
Cons: Hard to read/adjust mentally

RGB — Red, Green, Blue (The Logical Way)
Each channel is a number from 0 to 255.
css
.box-red {
  background-color: rgb(255, 0, 0);   /* Full red */
  color: rgb(255, 255, 255);           /* White */
  <!-- rgb(0,255,0)  Full green -->
  <!-- rgb(0,0,255) Blue -->
}

RGBA — RGB + Alpha (The Transparent Way)
Same as RGB, but with a 4th value: alpha (opacity) from 0.0 (invisible) to 1.0 (solid).
css
.box-red {
  background-color: rgba(255, 0, 0, 0.5);  /* 50% transparent red */
}
Use case: Overlays, glass effects, hover states, layering colors
