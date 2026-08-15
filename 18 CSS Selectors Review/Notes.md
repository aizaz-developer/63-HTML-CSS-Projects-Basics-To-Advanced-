 Project 18: CSS Selectors Quiz — Notes

## 1. Element Selector
Targets all instances of an HTML tag.

```css
p {
  color: blue;
}
```

## 2. Class Selector
Targets elements with a specific class. Reusable across many elements.

```css
.highlight {
  background-color: yellow;
}
```

## 3. ID Selector
Targets one unique element. IDs must be unique per page.

```css
#header {
  font-size: 2rem;
}
```

## 4. Descendant Selector
Targets an element inside another element (any level deep).

```css
nav a {
  text-decoration: none;
}
```

## 5. Grouping Selector
Apply the same styles to multiple selectors at once. Separate with commas.

```css
h1, h2, h3 {
  font-family: Georgia, serif;
}
```

## 6. Universal Selector
Targets EVERY element on the page. Commonly used for resets.

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
```

## Specificity Order (Low to High)
1. Universal `*` — lowest
2. Element `p` — low
3. Class `.btn` — medium
4. ID `#nav` — high
5. Inline style — highest