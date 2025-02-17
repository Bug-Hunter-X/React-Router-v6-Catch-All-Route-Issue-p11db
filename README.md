# React Router v6 Catch-All Route Bug

This repository demonstrates a subtle bug in React Router v6 related to the catch-all route (`/*`).  The issue occurs when the catch-all route unintentionally overrides more specific routes, leading to unexpected rendering behavior.

## Problem

In the provided example (`App.js`), the catch-all route (`/*`) is meant to handle 404 errors.  However, it is triggered even when navigating to other defined routes, such as `/about`.

## Solution

The solution (`AppSolution.js`) restructures the routes, prioritizing specific routes before the catch-all route. By moving `/*` to the end of the route definitions, the more specific routes are processed first, resolving the issue.