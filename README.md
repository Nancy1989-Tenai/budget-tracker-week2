# Budget Tracker — Week 2 Project

## What I Built

This is a **personal budget tracker** web page built with semantic HTML and CSS. It lets a user view a table of sample expenses, fill out a form to (eventually) add new ones, watch an embedded budgeting tips video, and read collapsible help instructions. The project was built on top of a Week 1 foundation and extended with proper table structure, an upgraded form, multimedia elements, and advanced CSS selectors.

---

## File Breakdown

### `index.html`

| Section | What It Does |
|---|---|
| **Header** | Displays the page title alongside a wallet icon (`<img>` with `src`, `alt`, and `width`). |
| **Add Expense Form** | A `<form>` wrapper containing labeled inputs for name, amount, category (`<select>` with 5 options), and date. Every input has a unique `id`. A `<button type="button">` is included for future JavaScript use. |
| **Expense Table** | A fully structured `<table>` with `<thead>` (column headers: Name, Amount, Category, Date) and `<tbody>` containing 5 rows of hardcoded sample data. |
| **Video Section** | An `<iframe>` embedding a YouTube budgeting tips video with `width`, `height`, `title`, and `frameborder` attributes. |
| **Help Section** | A `<details>` / `<summary>` collapsible block explaining how to use the tracker. |
| **Footer** | Simple copyright line. |

### `style.css`

| Feature | Details |
|---|---|
| **Reset & Base** | Universal box-sizing reset, body font and background. |
| **Form Styling** | Flexbox layout, rounded inputs, styled button with hover state. |
| **Table Styling** | `border-collapse: collapse`, cell padding, dark header row, alternating row colors via `tr:nth-child(even)`, and a hover highlight on rows. |
| **Advanced CSS Selectors** | See list below. |

### Advanced CSS Selectors Used

1. **Descendant selector** — `.expenses-section td` and `.expenses-section th` target table cells only inside the expenses section.
2. **Direct child selector** — `.add-expense-form > button` styles only the button that is a direct child of the form.
3. **Position-based pseudo-class** — `tr:nth-child(even)` creates alternating row backgrounds; `tr:first-child` removes the top border on the first data row.
4. **Negation pseudo-class** — `input:not([type="submit"])` styles all inputs except submit buttons.
5. **Focus pseudo-class** — `input:focus, select:focus` adds a blue glow ring when the user clicks into a field.

---

## How to View

1. Clone or download this repository.
2. Open `index.html` in any modern browser.
3. No build tools or dependencies are required.

---

## Grading Rubric Coverage

| Criterion | Where It's Met |
|---|---|
| Correct HTML Table Structure (25%) | `<table>`, `<thead>`, `<tbody>`, `<tr>`, `<th>`, `<td>` all used correctly with 5 data rows. |
| Working Form Upgrade (30%) | `<form>` wrapper, `<select>` with 5 options, `<button type="button">`, all inputs have matching `id` attributes. |
| Multimedia Elements (15%) | `<img>` with `src`/`alt`/`width`; `<iframe>` with `width`/`height`/`title`/`frameborder`. |
| Advanced CSS Selectors (30%) | Five selectors applied: descendant, direct child, nth-child/even, :not(), and :focus. |
