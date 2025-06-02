---
type: StrictMode
keywords: react, enquiry, StrictMode
tags: [react, enquiry, strictmode]
---

## StrictMode

```
<StrictMode>
  <App />
</StrictMode>
```
Use StrictMode to enable additional development behaviors and warnings for the component tree inside:

Strict Mode enables the following development-only behaviors:

- Your components will re-render an extra time to find bugs caused by impure rendering.
- Your components will re-run Effects an extra time to find bugs caused by missing Effect cleanup.
- Your components will re-run refs callbacks an extra time to find bugs caused by missing ref cleanup.
- Your components will be checked for usage of deprecated APIs.

Although the Strict Mode checks only run in development, they help you find bugs that already exist in your code but can be tricky to reliably reproduce in production. Strict Mode lets you fix bugs before your users report them.


### Pure function
A function will return same output every time same input.

In terms of react - React components you write must always return the same JSX given the same inputs (props, state, and context).


Components breaking this rule behave unpredictably and cause bugs. To help you find accidentally impure code, Strict Mode calls some of your functions (only the ones that should be pure) twice in development.

### How Strict mode helps?
StrictMode renders the pure function twice.
If both render produes same output then the function fine. If both render is different, then something wrong in the function. We can catch it in the development if StrictMode is used.
