# Shopback calculator assignment

## Description

In this assignment, I have structured the project such that the shopback-calculator.js acts as the entry point to the app, which would then use /src/index.js to route the input arguments entered in the command line to the correct path in the /src/actions directory through a switch statement.

The modularity of the code is ensured by separating the routing logic in /src/index.js from the business logic in the /src/actions directory. The data used to calculate the signup bonus or the redeem URL is kept in the /src/data directory, which would allow for easy modification of any parameters in the future.

There is handling of edge cases for invalid input, and Mocha is used to conduct unit testing, with the test suites stored in the /test directory. To conduct testing, simply type `npm test` at the root of the directory.

## Project structure

- shopback-calculator.js ────>  Entry point to the app
- **src**
  - index.js      ────>            Provides routing to different actions
  - **actions**
    - redeem.js  ────>           Business logic for redeem action
    - signup.js   ────>          Business logic for signup action
    - spend.js   ────>           Business logic for spend action
  - **data**
    -  bonus.js   ────>           Mapping of website to bonus amount for signup.js
    -  website.js ────>           Mapping of website to full URL name for redeem.js
- **test**
  - test.js        ────>           Test file for unit testing using Mocha
- package.json
- package-lock.json
- README.md


## How to add a new action

In order to extend a new action to the code, simply place the new code within the /src/actions folder, and add these additional lines of code to the switch statement in **index.js**.

```
case 'NEW_ACTION':
  res = require('./actions/NEW_ACTION')(args);
  break;
```

## Install

```
$ git clone ./calc.bundle
$ cd calc
$ npm install
```
