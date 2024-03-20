# Big Bang front end test

## Problem

Creating a dashboard using Vue.js, being as faithful as possible to the Figma sent for testing, and following the following instructions:

- I can use an icon library
- I can use a style library
- I must follow Clean code principles

As an additional, I am following the following principles:

- Short Commits
- Conventional Commits
- Single responsibility principle
- Clean architecture

## Techs Used

The technologies used are:

- Vue.js (mandatory),
- Typescript, to ensure everything is typed correctly,
- Font awesome, to use icons,
- Git Commit Msg Linter, to handle my commits

## How to run this code

### Cloning

To run this test code, you should follow these steps:

- Clone this repo, using ssh or hhtps url.  
  Using ssh :

```sh
git clone git@github.com:Ceagah2/bigbang-test.git
```

Using HTTPS:

```sh
https://github.com/Ceagah2/bigbang-test.git
```

After cloning the repo, you should navigate into it.

```sh
cd bigbang-test
```

### Installing

Once you're into the test folder, you should install the dependencies, using your favorite package manager.

PNPM:

```sh
pnpm install
```

NPM:

```sh
npm install
```

YARN

```sh
yarn
```

### Running

Once you already have installed, you should run.

Using PNPM :

```sh
pnpm run dev
```

Using NPM

```sh
npm run dev
```

Using YARN

```sh
yarn dev
```

## Final considerations

While developing the project, I encountered some issues with my favorite styling library, styled-components, and creating themes for the entire application's design system. Since time was short and I wanted to deliver a fully responsive application, I ended up abandoning the use of my preferred style to focus on project delivery.

Another thing I considered using, but was unsure about its behavior over time, is the CRUD application, which simulates a database, and I would only need to consume the endpoints. However, as mentioned earlier, I was uncertain about its behavior over time, and what was registered could disappear, leaving my application with zeroed data, thus losing its fidelity to the Figma design.

I really enjoyed developing this project, and I am happy with the outcome, even though I know it's not 100% of what I initially planned.
