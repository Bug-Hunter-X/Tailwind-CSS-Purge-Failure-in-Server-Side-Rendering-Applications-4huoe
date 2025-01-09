# Tailwind CSS Purge Failure in Server-Side Rendering

This repository demonstrates a common bug encountered when using Tailwind CSS with server-side rendering (SSR) frameworks like Next.js or Nuxt.js.  The problem arises from the purge process failing to identify all classes used dynamically, leading to missing styles.

## Problem

When components render conditionally or classes are used dynamically, Tailwind's purge may remove classes that are still referenced, causing runtime styling errors.

## Solution

The provided solution demonstrates several approaches to mitigate the issue:

- **Explicitly include classes:** Manually list all potential classes in the `purge` configuration.
- **Adjust Purge Options:** Modify the purge options to include content from various paths or adjust strategies.
- **Use `@apply` directives:** Applying styles with `@apply` ensures that referenced styles aren't purged.
- **Disable Purge:** Temporarily disable the purge process during development to identify all classes in use.