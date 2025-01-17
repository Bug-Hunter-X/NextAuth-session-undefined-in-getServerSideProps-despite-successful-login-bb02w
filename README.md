# NextAuth Session Undefined in getServerSideProps

This repository demonstrates a common issue encountered when using NextAuth.js with getServerSideProps: the session object is undefined, even after successfully logging in.  This leads to errors when trying to access user data within the session.

## Problem

The `getServerSideProps` function in the `pages/about.js` file attempts to access `session.user.email`. However, despite successful authentication through NextAuth, the `session` object is frequently undefined, resulting in a runtime error.

## Solution

The solution involves ensuring that the `authOptions` are correctly imported and used within `unstable_getServerSession`. The example provided corrects the import and provides proper error handling.

## Setup

1. Clone this repository.
2. Run `npm install` or `yarn install` to install dependencies.
3. Run `npm run dev` or `yarn dev` to start the Next.js development server.

This example utilizes NextAuth.js. You'll need to set up a NextAuth provider (like Email, Google, etc.) for it to work correctly.  Refer to the NextAuth.js documentation for configuration.