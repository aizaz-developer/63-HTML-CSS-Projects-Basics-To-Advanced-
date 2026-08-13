# Project 11: My First Styled Page

## What I Learned
- Three ways to add CSS: Inline, Internal, External
- CSS Selectors: element, class, id, descendant, grouping, universal
- The `&lt;link&gt;` tag connects external stylesheets
- The `style` attribute and `&lt;style&gt;` tag

## Files
- `index.html` — Page structure with all three CSS methods
- `style.css` — External stylesheet

## CSS Methods Used
| Method | Location | Example |
|--------|----------|---------|
| Inline | `style=""` attribute | `&lt;h1 style="color: #e74c3c;"&gt;` |
| Internal | `&lt;style&gt;` in `&lt;head&gt;` | `body { font-family: Arial; }` |
| External | `style.css` + `&lt;link&gt;` | `p { background-color: #f7f707; }` |

## Selectors Used
| Selector | Target | Code |
|----------|--------|------|
| `*` | All elements | Reset margin & padding |
| `h1, h2` | Grouped headings | Georgia font family |
| `p` | All paragraphs | Yellow background, rounded corners |
| `.header` | Header section | Pink background, centered |
| `.welcome` | Welcome heading | 32px font size |
| `.explore` | Explore heading | 24px, dark color |
| `#tech` | Tech paragraph | Blue text, 18px |
| `nav a` | Nav links only | Bold, no underline |

## Properties Practiced
- `color`, `background-color`
- `font-size`, `font-family`
- `text-align`, `text-decoration`
- `padding`, `margin`
- `border-radius`