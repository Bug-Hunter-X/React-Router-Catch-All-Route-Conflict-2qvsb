# React Router Catch-All Route Conflict

This repository demonstrates a common issue with React Router's catch-all route (`/*`). When placed before other routes, it can incorrectly intercept requests intended for other paths, resulting in unexpected page rendering and routing problems.

## Bug Description
The provided `App.js` uses React Router's `Routes` component to define routes.  The catch-all route (`/*`) is placed above other, more specific routes.  This causes the catch-all route to always match and renders the NotFound component even for valid routes like `/` and `/about`.

## Solution
The solution in `AppSolution.js` reorders the routes to place the catch-all route last.  This ensures that more specific routes are matched before the catch-all route, correctly rendering the pages.