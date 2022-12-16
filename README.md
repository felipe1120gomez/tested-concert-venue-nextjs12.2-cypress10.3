# Popular Concert Venue

### An app to support the Udemy course [Testing Next.js Apps](https://www.udemy.com/course/nextjs-testing/)

## Installation and Scripts

1. Run `npm install`
1. For Jest Tests Run `npm test`
1. Before running Cypress for the first time and after every change in the App Run `npm run build:test`
1. Cypress on the command line Run `npm run cypress:run`
1. Cypress in the browser Run `npm run cypress:start`

## Running the App

Run `npm run dev`. The app will be found at [http://localhost:3000]

## Alternative scripts for linux based systems

### 0nly use if the current ones do not work

```rb
"scripts": {
    "db:reset": "source scripts/reset-db.sh",
    "dev": "next dev",
    "lint": "next lint",
    "build": "next build",
    "build:test": "npm run db:reset && export NODE_ENV=\"test\" && next build",
    "start": "next start",
    "start:test": "export NODE_ENV=\"test\" && next start",
    "test": "jest --watch",
    "test:ci": "jest --ci",
    "cypress:open": "env-cmd -f .env.test.local cypress open",
    "cypress:start": "start-server-and-test 'npm run start:test' 3000 'npm run cypress:open'",
    "cypress:build": "npm run build:test && npm run cypress:start",
    "cypress:run": "start-server-and-test 'npm run start:test' 3000 'env-cmd -f .env.test.local cypress run'"
  },
```
