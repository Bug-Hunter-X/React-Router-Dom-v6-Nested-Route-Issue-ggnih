# React Router Dom v6 Nested Route Bug

This repository demonstrates a bug in React Router Dom v6 where nested routes fail to render correctly. The catch-all route (`/*`) incorrectly matches, overriding nested route definitions.

## Bug Description
Nested routes within a parent route are not displayed. Instead, the catch-all route (`/*`) renders, masking the content of the nested routes.

## Steps to Reproduce
1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe that navigating to a nested route doesn't display the correct content. The 'Not Found' page is displayed instead.

## Solution
The solution involves correctly structuring the routes to avoid route conflicts with the catch-all route.  Ensure the catch-all route is only for actual 'not found' cases, not for inadvertently catching valid nested paths.