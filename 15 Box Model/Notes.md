 Concepts
Every HTML element is a box. Understanding how that box is built is the most important skill in CSS layout. The box has 4 layers, from inside to outside:
plain
┌─────────────────────────────┐
│          MARGIN             │  ← outer space (transparent)
│   ┌─────────────────────┐   │
│   │       BORDER        │   │  ← visible edge
│   │   ┌─────────────┐   │   │
│   │   │   PADDING   │   │   │  ← inner space (background shows)
│   │   │   ┌─────┐   │   │   │
│   │   │   │CONTENT│   │   │   │  ← text, images, etc.
│   │   │   └─────┘   │   │   │
│   │   └─────────────┘   │   │
│   └─────────────────────┘   │
└─────────────────────────────┘
1. content — The Innermost Layer
This is your actual text, images, or nested elements. Its size is controlled by width and height.
css
.box {
  width: 200px;
  height: 100px;
}
Trap: By default, width and height set the content size only. Padding and border are added outside that, making the total element bigger than you specified.
2. padding — Space Inside the Border
Padding pushes the content away from the border. It uses the element's background color.
css
.box {
  padding: 20px;           /* all 4 sides */
  padding: 10px 20px;      /* top/bottom 10px, left/right 20px */
  padding: 10px 20px 30px 40px; /* top right bottom left */
  
  /* Or target one side */
  padding-top: 10px;
  padding-left: 15px;
}
Key rule: Padding adds space inside the box. It increases the total size unless you use box-sizing: border-box.
3. border — The Visible Edge
The border sits between padding and margin. You control its width, style, and color.
css
.box {
  border-width: 4px;
  border-style: solid;     /* solid, dashed, dotted, double, etc. */
  border-color: #333333;
  
  /* Shorthand */
  border: 4px solid #333333;
  
  /* One side only */
  border-bottom: 2px dashed red;
}
4. margin — Space Outside the Border
Margin pushes other elements away. It is always transparent.
css
.box {
  margin: 20px;            /* all sides */
  margin: 10px auto;       /* top/bottom 10px, left/right auto (centers horizontally) */
  
  /* One side */
  margin-top: 30px;
  margin-bottom: 15px;
}
Key rule: Margins can collapse. If two block elements touch vertically, the larger margin wins — they don't add up. Example: a box with margin-bottom: 30px above a box with margin-top: 20px creates only 30px of space, not 50px.
5. box-sizing — The Game Changer
By default, browsers use content-box. This means:
plain
Total width = width + padding-left + padding-right + border-left + border-right
This is annoying. The fix is border-box:
css
/* Put this at the top of every CSS file */
* {
  box-sizing: border-box;
}
With border-box:
plain
Total width = width (padding and border are INCLUDED)
Always use border-box. It makes width and height behave the way you intuitively expect.
6. Visualizing the Box Model
To see the layers clearly, developers use different background colors:
css
.content {
  background-color: lightblue;   /* content */
  padding: 20px;
  background-color: lightgreen;  /* padding area */
  border: 5px solid orange;      /* border */
  margin: 30px;
  /* margin is invisible — no background */
}