# Vue 3 Project Setup Guide

## ᴹᴹᴹ 1. Prerequisites

Ensure the following tools are installed:

* **Node.js** (LTS version): [https://nodejs.org](https://nodejs.org)
* **npm** (comes with Node) or **Yarn**
* **Vite** (preferred over Vue CLI for Vue 3)

---

## 🚀 2. Project Initialization with Vite

### Using npm:

```bash
npm create vite@latest my-vue-app -- --template vue
cd my-vue-app
npm install
```

### Using Yarn:

```bash
yarn create vite my-vue-app --template vue
cd my-vue-app
yarn
```

---

## 🏗️ 3. Recommended Project Structure

```
src/
├── assets/         # Static assets (images, logos, etc.)
├── components/     # Reusable components
├── views/          # Page-level views (for Vue Router)
├── composables/    # Reusable logic (Composition API)
├── router/         # Vue Router setup
├── store/          # Pinia or Vuex (for global state)
├── services/       # API calls and business logic
├── utils/          # Utility functions
├── App.vue
└── main.js
```

---

## ⚙️ 4. Install Essential Dependencies

### State Management:

```bash
npm install pinia
```

In `main.js`:

```js
import { createPinia } from 'pinia';
app.use(createPinia());
```

### Routing:

```bash
npm install vue-router
```

Set up in `src/router/index.js`.

### HTTP Client:

```bash
npm install axios
```

Centralize API calls in `services/`.

---

## 🧚‍♂️ 5. Developer Tools & Linting

### ESLint + Prettier:

```bash
npm install -D eslint prettier eslint-plugin-vue eslint-config-prettier
```

Configure `.eslintrc.cjs` and `.prettierrc`.

### Optional: TypeScript

```bash
npm install -D typescript
```

Rename `main.js` to `main.ts` and configure `tsconfig.json`.

---

## 🧰 6. Recommended Plugins

* **VueUse**: `npm install @vueuse/core`
* **Vite Plugins**:

  * `vite-plugin-vue-layouts`
  * `vite-plugin-pages`
* **Vue Router Devtools**

---

## 🔍 7. Development & Testing

Run dev server:

```bash
npm run dev
```

Install **Vitest** for testing:

```bash
npm install -D vitest vue-test-utils
```

---

## ✅ 8. Git & CI Setup

* Initialize Git: `git init`
* Add `.gitignore`
* Configure GitHub Actions or GitLab CI if needed

---

## 📦 9. Build and Deploy

To build for production:

```bash
npm run build
```

Deploy the `/dist` folder using services like Netlify, Vercel, or traditional hosting.

---

## 🗰️ Final Tips

* Use **Composition API** throughout (`setup()`, `ref`, `computed`, etc.)
* Keep components **small and focused**
* Modularize logic into `composables` and `services`
* Use **lazy loading** in Vue Router

---

Happy coding with Vue 3! 🌟
