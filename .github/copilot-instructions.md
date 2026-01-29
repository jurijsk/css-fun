
- **Styling:** CSS conventions for this workspace
  - Use modern, plain CSS for all styling. Do not add CSS frameworks (Tailwind, Bootstrap, etc.) unless you have explicit approval. Do not use pre and post processort such as SCSS.
  - Prefer component-scoped `<style>` blocks to avoid global leakage in files under `app/components`.
  - Prefer type selectors for high-level layout when semantically appropriate (e.g., `main`, `header`, `footer`, `nav`, `section`).
  - **CSS class naming:** When a class selector is required, use semantic names that describe what the element *is* or *does*, not its location in the DOM hierarchy with snake_case.  Do not use BEM-style or kebab-case naming. 
  - Keep selectors specific but minimal — aim for clear structure over deeply nested selectors.
  - Follow simple, maintainable conventions (CSS variables, logical class names). 
  - Use variables or design tokens for colors/spacing when available; otherwise use small, consistent values.