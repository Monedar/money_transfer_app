# ActionMoneyTransfer

## Prerequisites

The build process is a series of Gulp tasks and the HTTP server used is an NPM module.  Because of this [NodeJS](https://nodejs.org/en/download/) is a prerequisites for working on this codebase.

## Setup

Once you have the prerequisites installed and the repository cloned run the following command to install all dependent NPM modules and type definitions:

```
npm install
```

## Running HTTP Server

```
npm start
```

## Running Tests

To run tests once:

```
npm test
```

To run tests continually as your are developing:
```
npm run watch:test
```

## Directory Structure

Overview

    ├── dist                              - all of the compiled source code that comes out of the build process
    ├── src                               - directory housing all source code
    │   ├── index.html                    - main index.html page
    │   ├── app                           - all custom development files will go somewhere under 
    │   │   ├── account.model.ts          - class defining a account
    │   │   ├── account.service.ts        - service functions for functionality regarding accounts
    │   │   ├── account.service.spec.ts   - tests for functions in account.service.ts
    │   │   ├── accountCard.html          - component template for accountCard.component.ts
    │   │   ├── accountCard.component.ts  - component that renders a card representing an account
    │   │   ├── addAccount.html           - HTML template servicing the addAccount modal popup
    │   │   ├── addAccount.ts             - controller servicing the addAccount modal popup
    │   │   ├── app.module.ts             - the main module file where the 'app' module is defined and all dependent modules are registered
    │   │   ├── app.component.ts          - the root component for the application
    │   │   │                                * this component contains the main set of data (accounts) for the application and exposes the functions that are used to maintain them
    │   │   │                                * the property containing the set of accounts and the functions are then passed down to other components to use
    │   │   ├── app.config.ts             - application configuration settings
    │   │   ├── notifiation.service.ts    - service functions that create messages for the users
    │   │   ├── sideColumn.html           - HTML template for sideColumn.component.ts
    │   │   ├── sideColumn.component.ts   - component representing the side column of the layout
    │   │   ├── toolbar.html              - HTML template for toolbar.component.ts
    │   │   ├── toolbar.component.ts      - component representing the toolbar at the top of the layout 
    │   ├── assets                        - all styles and image content should be placed under this directory
    │   │   ├── app.css                   - custom LESS
