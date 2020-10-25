# Testing-Nuxt

## Creating our Nuxt App
```bash
# install using Yarn
$ yarn create nuxt-app <project-name>

# install using npx
$ npx create-nuxt-app <project-name>
```
It will ask you some questions (name, Nuxt options, UI framework, TypeScript, linter, testing framework, etc. 

[<img src="https://firebasestorage.googleapis.com/v0/b/vue-mastery.appspot.com/o/flamelink%2Fmedia%2F1578373049722_0.jpg?alt=media&token=7b4174b7-b15b-434b-9dc2-9dd4253b32fe" width="50%">]()

To find out more about all the options see the [Create Nuxt app](https://github.com/nuxt/create-nuxt-app/blob/master/README.md).

## Launch Nuxt

```bash
cd <project-name>

# install dependencies
$ yarn install

# serve with hot reload at localhost:3000
$ yarn dev

# build for production and launch server
$ yarn build
$ yarn start

# generate static project
$ yarn generate
```

## Nuxt Folder Structure

You’ll first notice that Nuxt.js has no /src directory, these folder are in root.

[<img src="https://firebasestorage.googleapis.com/v0/b/vue-mastery.appspot.com/o/flamelink%2Fmedia%2F1578373066655_5.jpg?alt=media&token=c5fed040-8bc9-4bfe-8333-ac580c180fea" width="50%">]()

How does Nuxt render Vue pages/layouts and components?

[<img src="https://firebasestorage.googleapis.com/v0/b/vue-mastery.appspot.com/o/flamelink%2Fmedia%2F1578373061939_3.jpg?alt=media&token=2475f5b7-591f-46b9-9087-1aea19903af5" width="50%">]()

Each of these folders will contain component .vue files, and they each start out with a single default generated file, which together showed us the page we saw when we launched the development server.

[<img src="https://firebasestorage.googleapis.com/v0/b/vue-mastery.appspot.com/o/flamelink%2Fmedia%2F1578373064141_4.jpg?alt=media&token=40f2e214-094f-4140-91aa-e35ac64a508f" width="50%">]()

## SPA versus Universal Mode

### Typical Vue SPA

[<img src="https://firebasestorage.googleapis.com/v0/b/vue-mastery.appspot.com/o/flamelink%2Fmedia%2F1578373459127_0.jpg?alt=media&token=86e8ecca-a0ae-494c-bf7f-a97c09b36a70" width="50%">]()

### Universal Mode

Universal Mode, which means that when the application is initially loaded, it will render the page requested on the server-side first, before sending over the initial HTML.

[<img src="https://firebasestorage.googleapis.com/v0/b/vue-mastery.appspot.com/o/flamelink%2Fmedia%2F1578373459128_1.jpg?alt=media&token=a64e156d-8805-44a8-b57b-b41a3a1c5c46" width="50%">]()

The new page is shown before downloading and running any JavaScript. Once JavaScript is downloaded and run Vue is started up and the page “Hydrated,” which basically means it turns into a normal SPA (Single Page App).


For detailed explanation on how things work, check out [Nuxt.js docs](https://nuxtjs.org).

Credits to [Vue Mastery](https://www.vuemastery.com/)
