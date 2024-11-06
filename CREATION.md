# The process used to create the Nuggets project

## Use Node 20

Assumes nvm is used to manage Node.

```sh
nvm use 20
```

## Use PNPM

```sh
pnpm init
```

## Create a Quasar SPA app

```sh
pnpm create quasar
```

Choices:
```sh
✔ What would you like to build? › App with Quasar CLI, let's go!
✔ Project folder: … app
✔ Pick Quasar version: › Quasar v2 (Vue 3 | latest and greatest)
✔ Pick script type: › Javascript
✔ Pick Quasar App CLI variant: › Quasar App CLI with Vite 2 (stable | v1)
✔ Package name: … app
✔ Project product name: (must start with letter if building mobile apps) … Nuggets
✔ Project description: … Manage the nuggets of data in your life
✔ Author: … Brian Winkers <winkersbrian@gmail.com>
✔ Pick a Vue component style: › Composition API with <script setup>
✔ Pick your CSS preprocessor: › Sass with SCSS syntax
✔ Check the features needed for your project: › Linting (vite-plugin-checker + ESLint), State Management (Pinia), axios, vue-i18n
✔ Pick an ESLint preset: › Prettier
```

## Integrate SuperTokens with Vue

### Use supertokens-web-js module

```sh
pnpm install supertokens-web-js
```

### Create a free, hosted SuperTokens account

