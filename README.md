# React Router Dom Route Order Issue

This repository demonstrates a common error in React Router Dom v6 where the order of routes in the `<Routes>` component affects the matching logic.

Specifically, if a catch-all route (`*`) is placed before more specific routes, the catch-all route will always be matched, and the other routes will never be reached. This is because React Router matches routes from top to bottom.

The solution is to move the catch-all route to the end of the `<Routes>` component, after all other more specific routes. This ensures that more specific routes will be matched before the catch-all route.

## Bug

The file `App.js` shows a typical example of this problem, where the `/contact` route will never be matched because the `*` route is above it.  

## Solution

The solution is in `AppSolution.js` which corrects the route order to prioritize specific routes over the catch-all. 