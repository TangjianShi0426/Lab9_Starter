# Copilot Instructions for Lab9_Starter

- This is a minimal static web project. The only application entry point is `index.html`.
- There is no build system, package manager, or test harness present in the repository.
- Changes should be made directly to `index.html`, including HTML structure, inline CSS, and inline JavaScript.

## What this project does

- Implements a simple calculator form and a set of buttons that demonstrate browser console APIs.
- `index.html` contains:
  - a calculator form with validation and `try/catch/finally`
  - a `ValidationError` subclass used for missing input
  - examples of `console.log`, `console.error`, `console.warn`, `console.count`, `console.assert`, `console.group`, `console.table`, `console.time`, `console.trace`
  - a global error handler via `window.onerror` and `window.addEventListener('error', ...)`
- The demo is intended to show JavaScript error handling and console behavior.

## Key patterns and implementation notes

- All JavaScript lives inline inside `<script>` at the bottom of `index.html`.
- DOM queries use `document.querySelector` and `document.querySelectorAll`.
- Event handling is added directly to elements like the form and buttons.
- The calculator uses `eval()` with user input; any change to arithmetic logic should preserve input validation and error handling.
- `ValidationError` is used to signal missing number input and is logged to the console on catch.

## If you add features

- Keep the page self-contained unless the task explicitly asks for external files.
- If you split logic into separate JS/CSS files, update `index.html` accordingly with `<script src="...">` or `<link rel="stylesheet" ...>`.
- Maintain the browser-first behavior: open `index.html` in a browser to verify functionality.

## Running and verifying

- There is no `npm`, `yarn`, or automated runner.
- Verify changes by opening `index.html` in a browser and using the developer console.
- The active demo is the calculator form and the console buttons under `#error-btns`.

## What not to do

- Do not assume a backend or API exists; this repo is purely static.
- Do not add unrelated tooling, tests, or dependencies unless the task explicitly requires it.
- Do not remove the global error handling patterns without preserving equivalent error reporting.
