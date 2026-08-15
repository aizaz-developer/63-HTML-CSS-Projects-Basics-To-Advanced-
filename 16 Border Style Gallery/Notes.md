Concepts
Today we master the 4 border properties: border-width, border-style, border-color, and border-radius.
1. border-width — How Thick the Border Is
Controls the thickness of the border line.
border-width — How Thick the Border Is
Controls the thickness of the border line.
css
.thin {
  border-width: 1px;
}

.medium {
  border-width: 4px;
}

.thick {
  border-width: 8px;
}

.very-thick {
  border-width: 16px;
}
You can also set sides individually:
css
.mixed-width {
  border-top-width: 2px;
  border-right-width: 6px;
  border-bottom-width: 10px;
  border-left-width: 14px;
}
2. border-style — How the Border Looks
This is required for a border to show. Without it, no border appears even if you set width and color.
css
.solid {
  border-style: solid;      /* a straight line */
}

.dashed {
  border-style: dashed;     /* ----- */
}

.dotted {
  border-style: dotted;     /* ...... */
}

.double {
  border-style: double;     /* two parallel lines */
}

.groove {
  border-style: groove;     /* 3D carved in */
}

.ridge {
  border-style: ridge;      /* 3D pushed out */
}

.inset {
  border-style: inset;      /* looks embedded */
}

.outset {
  border-style: outset;     /* looks raised */
}

.none {
  border-style: none;       /* no border */
}

.hidden {
  border-style: hidden;     /* invisible but takes up space */
}
The most common styles: solid, dashed, dotted, double. The 3D ones (groove, ridge, inset, outset) look dated but are still valid CSS.
3. border-color — The Border's Color
Any valid color value works: name, hex, rgb, rgba.
css
.red-border {
  border-color: #ff0000;
}

.blue-border {
  border-color: rgb(0, 123, 255);
}

.transparent-border {
  border-color: transparent; /* invisible but keeps layout */
}

.multi-color {
  border-top-color: red;
  border-right-color: green;
  border-bottom-color: blue;
  border-left-color: orange;
}
4. Shorthand — border
Instead of writing 3 separate properties, use the shorthand:
css
.box {
  border: 4px solid #333333;
  /*      width  style   color  */
}
Order does not matter, but the convention is width → style → color.
5. border-radius — Rounded Corners
Rounds the corners of the border box.
css
.slight-round {
  border-radius: 4px;
}

.medium-round {
  border-radius: 12px;
}

.fully-round {
  border-radius: 50%;       /* makes a circle if width = height */
}

.pill-shape {
  border-radius: 999px;     /* creates a pill/capsule shape */
}

/* Different corners */
.custom-corners {
  border-top-left-radius: 10px;
  border-top-right-radius: 20px;
  border-bottom-right-radius: 30px;
  border-bottom-left-radius: 40px;
}

/* Shorthand: top-left, top-right, bottom-right, bottom-left */
.all-at-once {
  border-radius: 10px 20px 30px 40px;
}
6. border-radius with 2 Values (Elliptical Corners)
You can make corners elliptical by giving 2 values per corner:
css
.ellipse {
  border-radius: 20px / 40px;
  /* horizontal radius / vertical radius */
}
This creates rounded corners that are wider than they are tall.