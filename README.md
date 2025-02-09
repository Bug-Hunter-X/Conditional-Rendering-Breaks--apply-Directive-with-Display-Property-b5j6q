# Conditional Rendering Breaks @apply Directive with Display Property

This repository demonstrates a bug where Tailwind CSS's `@apply` directive fails to correctly apply styles when a component using it is conditionally rendered.  Specifically, the issue is observed when the `@apply` directive includes a utility class that modifies the `display` property (e.g., `flex`, `block`, `inline-block`).

The bug is likely due to a timing issue or the way Tailwind processes the directives within the conditional rendering context.  The provided solution showcases a workaround that ensures proper style application.

## Steps to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm run serve` to start the development server.
4. Observe the behavior of the conditionally rendered component.

## Bug and Solution

See `ConditionalRenderingBug.vue` for the code that demonstrates the bug and `ConditionalRenderingSolution.vue` for a solution.  The solution involves a simple change that forces the component to render its styles correctly.