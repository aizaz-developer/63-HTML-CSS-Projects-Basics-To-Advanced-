The Three Ways to Add CSS
There are three ways to apply CSS to HTML. Think of them as "where do I put my paint?"
A. Inline CSS (Paint directly on the element)
You add a style attribute directly inside the HTML tag.
HTML
<h1 style="color: blue; font-size: 32px;">Hello World</h1>
Pros: Quick, overrides everything else
Cons: Messy, hard to maintain, repeats code
When to use: Almost never (only quick tests)

B. Internal CSS (Paint palette inside the page)
You write CSS inside a <style> tag in the <head>.
HTML
<head>
  <style>
    h1 {
      color: blue;
      font-size: 32px;
    }
  </style>
</head>
Pros: Good for single-page projects
Cons: CSS is trapped in this one file
When to use: Small projects, prototypes
C. External CSS (Paint palette in a separate file)
You write CSS in a separate .css file and link it with <link>.
index.html:
HTML
<head>
  <link rel="stylesheet" href="styles.css">
</head>
styles.css:
css
h1 {
  color: blue;
  font-size: 32px;
}
Pros: Clean, reusable across many pages, industry standard
Cons: One extra file to manage
When to use: Always, for real projects

CSS Selectors
Selectors are how you target HTML elements to style them.
Table
Selector	Symbol	Targets	Example
Element	none	All tags of that type	h1 { }
Class	.	Elements with that class	.card { }
ID	#	One unique element	#header { }
Descendant	space	Nested elements	nav a { }
Grouping	,	Multiple at once	h1, h2 { }
Universal	*	Everything	* { }
css
/* Element selector — all paragraphs */
p {
  color: gray;
}

/* Class selector — any element with class="highlight" */
.highlight {
  background-color: yellow;
}

/* ID selector — the ONE element with id="title" */
#title {
  font-size: 48px;
}

/* Descendant — only links inside nav */
nav a {
  text-decoration: none;
}

/* Grouping — h1 AND h2 AND h3 */
h1, h2, h3 {
  font-family: Arial, sans-serif;
}

/* Universal — EVERYTHING */
* {
  margin: 0;
  padding: 0;
}