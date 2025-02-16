# Next.js 15: useRouter Hook Error in getServerSideProps

This repository demonstrates a common error in Next.js 15 applications involving the use of the `useRouter` hook within the `getServerSideProps` function.  This hook is client-side and is not available during server-side rendering.  The provided solution shows the correct approach to navigate or access route information in `getServerSideProps`.

## Problem

Attempting to use `useRouter` inside `getServerSideProps` results in undefined behavior or errors, as the hook relies on client-side execution context.

## Solution

To correctly handle routing logic within `getServerSideProps`, use context provided by `getServerSideProps` itself, or utilize a different approach that doesn't rely on client-side hooks.