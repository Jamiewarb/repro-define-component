# define-component

This repo is a reproduction of a bug I'm getting with Nuxt Bridge.

This repo was created following these instructions:

1. Create a fresh Nuxt 2 project `yarn create nuxt-app define-component`
2. Upgrade to Nuxt Bridge following this guide: https://v3.nuxtjs.org/getting-started/bridge/
3. Add a Test.vue component to `~/components`
4. Add an input and a button, and give them `@change` and `@click.prevent` events respectively.
5. The handler for these events doesn't matter, but I made them call a method on the component.

## The Error

To get the error:

- Run `yarn dev` and open localhost:3000 in a browser.
- Observe the error "defineComponent is not defined".

![image](https://user-images.githubusercontent.com/2754728/146798150-710ef71d-7cac-4937-ab68-3e60b20958dd.png)


To circumvent the error:

- Remove either the entire `<input>` element or the entire `<button>` element.
- Open localhost:3000 in a browser.
- Observe the error no longer displays.

The docs say you can also import from `#imports` directly, but this gives another error:

- Add `import { defineComponent } from '#imports';` inside the `<script>` tag
- Observe `Module parse failed: Identifier 'defineComponent' has already been declared (10:9)` error in terminal
