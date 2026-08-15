Project 19: Hover & Focus Lab

1. :hover — When the Mouse is Over an Element
The :hover pseudo-class applies styles when the user's mouse pointer is sitting on top of an element. It works on links, buttons, divs, images — anything.
css
a:hover {
  color: red;
  text-decoration: underline;
}

button:hover {
  background-color: #333;
  color: white;
}
Key rules:
:hover only works on devices with a pointer (mouse, trackpad). It does nothing on touchscreens until you tap.
Always provide a visible change — color shift, underline, shadow, scale. Users need feedback.
The element before the colon is the normal state. The :hover is the interactive state.
css
/* Normal state */
.btn {
  background-color: blue;
  color: white;
}

/* Mouse-over state */
.btn:hover {
  background-color: darkblue;
  transform: translateY(-2px); /* subtle lift effect */
}
2. :focus — When an Element is Selected (Keyboard or Click)
The :focus pseudo-class applies when an element receives focus. This happens when:
A user clicks into an input field
A user tabs to a link or button with their keyboard
A user clicks a button
css
input:focus {
  border-color: #4d96ff;
  outline: none;          /* removes default browser outline */
  box-shadow: 0 0 0 3px rgba(77, 150, 255, 0.3);
}

a:focus {
  outline: 2px solid orange;
}
Why outline matters for accessibility:
Browsers add a default outline (usually a blue or dotted ring) around focused elements so keyboard users can see where they are. Never remove outline without replacing it — visually impaired users navigate entirely by keyboard.
Good practice:
css
/* Remove ugly default, add a better custom one */
input:focus {
  outline: none;
  border: 2px solid #4d96ff;
  box-shadow: 0 0 0 3px rgba(77, 150, 255, 0.2);
}
3. :active — The Moment of Click
The :active pseudo-class applies only while the user is actively pressing down on an element. It fires between :hover (mouse is over) and the click release.
css
button:active {
  transform: scale(0.96);   /* button presses down slightly */
  background-color: #222;
}
The order matters. If you write :hover and :active on the same element, the correct order in your CSS is:
css
/* 1. Normal */
.btn { }

/* 2. Hover */
.btn:hover { }

/* 3. Active */
.btn:active { }

/* 4. Focus (if needed) */
.btn:focus { }
This is called LVHA order for links: :link, :visited, :hover, :active. For buttons, hover → active → focus is the safe sequence.
4. cursor — Change the Mouse Pointer
The cursor property changes what the mouse looks like when it's over an element.
css
/* Default arrow */
.box { cursor: default; }

/* Hand pointer — for clickable things */
a, button { cursor: pointer; }

/* Text I-beam — for selectable text */
p { cursor: text; }

/* Not allowed — for disabled buttons */
button:disabled { cursor: not-allowed; }

/* Crosshair — for precise selection */
.crop-tool { cursor: crosshair; }

/* Move — for draggable items */
.draggable { cursor: move; }

/* Wait — loading state */
.loading { cursor: wait; }
Rule of thumb:
Links and buttons → cursor: pointer
Disabled buttons → cursor: not-allowed
Everything else → leave it alone unless you have a specific reason
5. outline — The Focus Ring
outline is like border, but it sits outside the border and does not affect the box size or layout. Browsers use it automatically for focused elements.
css
/* Default browser outline (varies by browser) */
input:focus {
  outline: 2px solid blue;
}

/* Custom outline */
input:focus {
  outline: 3px dashed orange;
  outline-offset: 4px;    /* gap between element and outline */
}

/* Remove outline (DANGEROUS for accessibility) */
input:focus {
  outline: none;
}
Properties:
outline-width — thickness (px)
outline-style — solid, dashed, dotted, double
outline-color — any color
outline-offset — space between the element edge and the outline
Shorthand:
css
input:focus {
  outline: 2px solid #4d96ff;
}
6. Combining Pseudo-Classes
You can chain pseudo-classes for precise control:
css
/* Only when hovered AND focused */
button:hover:focus {
  box-shadow: 0 0 10px gold;
}

/* Disabled button — no hover effect */
button:hover:disabled {
  background-color: gray;  /* won't apply because :disabled overrides */
}
7. The Full Interactive Lifecycle
Here's what happens when a user clicks a button:
Table
User Action	State Applied
Mouse moves over button	:hover
Mouse button pressed down	:hover + :active
Mouse button released	:focus (button stays focused)
Mouse moves away	Normal state
User presses Tab	:focus moves to next element

