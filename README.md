# nuxt starter

## Build Setup

```bash
# install dependencies
$ yarn install | npm install

# serve with hot reload at localhost:3000
$ yarn dev | npm run dev

# build for production and launch server
$ yarn build | npm run build
$ yarn start | npm run start

# generate static project
$ yarn generate | npm run generate

```

For detailed explanation on how things work, check out [documentation](https://nuxtjs.org).

---

## Step of Intalling Tailwind CSS for Nuxt 2

- https://tailwindcss.com/docs/guides/nuxtjs#2
- https://stackblitz.com/github/nuxt/starter/tree/v2-stackblitz?file=README.md

### Step 1

```
$ yarn create nuxt-app starter-nuxt2-tailwind | npx create-nuxt-app starter-nuxt2-tailwind | npm init nuxt-app starter-nuxt2-tailwind
$ cd starter-nuxt2-tailwind
```

### Step 2

```
$ yarn add --dev tailwindcss postcss autoprefixer | npm install -D tailwindcss postcss autoprefixer
$ npx tailwindcss init
$ npm audit fix --force
```

### Step 3

```
# Edit nuxt.config.js
export default {
  build: {
    postcss: {
      postcssOptions: {
        plugins: {
          tailwindcss: {},
          autoprefixer: {},
        },
      },
    },
  }
}
```

### Step 4

```
# Edit tailwind.config.js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: [
    "./components/**/*.{js,vue,ts}",
    "./layouts/**/*.vue",
    "./pages/**/*.vue",
    "./plugins/**/*.{js,ts}",
    "./nuxt.config.{js,ts}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

### Step 5

```
# Create assets/css/main.css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

### Step 6

```
# Edit nuxt.config.js
export default {
  css: [
    '@/assets/css/main.css',
  ],
}
```

### Step 7

```
# Create / Edit pages/index.vue
<template>
  <h1 class="text-3xl font-bold underline">
    Hello world!
  </h1>
</template>

# Run the application
$ npm run dev
```

For detailed explanation on how things work, check out [Nuxt.js docs](https://nuxtjs.org).
