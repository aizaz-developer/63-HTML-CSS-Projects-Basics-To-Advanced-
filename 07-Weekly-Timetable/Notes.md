# Project 07 Notes: HTML Tables

---

## 1. The `<table>` Tag

**What it is:** The container element that defines a data table — rows and columns of structured information.

**Code snippet:**
```html
<table border="1" cellpadding="10" cellspacing="0">
  <!-- table content -->
</table>
Common attributes:
border — thickness of the border around cells (use CSS later, but works in HTML for now)
cellpadding — space inside each cell
cellspacing — space between cells
When to use it:
Timetables and schedules
Financial data or spreadsheets
Comparison charts
Any data that fits a grid structure
2. <thead>, <tbody>, and <tfoot>
What they are: Semantic containers that group table rows by purpose.
Table
Tag	Purpose
<thead>	Header rows (column labels)
<tbody>	Main data rows
<tfoot>	Footer rows (totals, summaries)
Code snippet:
HTML
<table>
  <thead>
    <tr>
      <th>Time</th>
      <th>Monday</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>08:00</td>
      <td>Math</td>
    </tr>
  </tbody>
</table>
Why use them:
Screen readers can navigate header vs body independently
CSS can style headers differently without extra classes
If the table spans multiple pages when printing, <thead> repeats on each page
3. <tr>, <th>, and <td>
Table
Tag	Name	Purpose
<tr>	Table Row	A horizontal row of cells
<th>	Table Header	A header cell — bold and centered by default
<td>	Table Data	A standard data cell
Code snippet:
HTML
<tr>
  <th>Time</th>
  <th>Monday</th>
</tr>
<tr>
  <td>08:00</td>
  <td>Math</td>
</tr>
When to use <th> vs <td>:
Use <th> for column headers and row headers
Use <td> for all regular data cells
4. The colspan Attribute
What it is: Makes a single cell span across multiple columns horizontally.
Code snippet:
HTML
<tr>
  <td colspan="5" align="center">Lunch Break</td>
</tr>
How it works:
colspan="5" means this one cell takes up the space of 5 normal cells
The row containing this cell should have fewer <td> tags to compensate
align="center" centers the text (HTML attribute — use CSS later)
When to use it:
Merged header cells
Break rows like "Lunch Break" or "Holiday"
Summary rows that apply to all columns
Key Takeaways
<table> wraps everything; <thead> and <tbody> add semantic structure
<tr> = row; <th> = header cell; <td> = data cell
colspan merges cells across columns; there is also rowspan for vertical merging
Tables should be used for tabular data, NOT for page layout (use flexbox/grid for layout)
