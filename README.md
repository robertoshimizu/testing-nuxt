# What is Nuxt?
`NuxtJS` is a framework that helps you build *server-rendered* `Vue.js` applications easily. It abstracts most of the complex configuration such as server side rendering, automatically generated routes, improved meta tags managing and SEO improvement.

Working on the server side does not mean `NuxtJS` is a backend framework like Express. Server-side `NuxtJS` is actually a pre-configured vue server renderer.

## Why would you use Nuxt.js over Vue?
`NuxtJS` offers many benefits to front-end developers, but there was one key feature that make frontend developers to use this framework final – SEO improvement. 

Nuxt.js has great meta tags managing, so we could easily make specific and customisable social share windows depending on the data received from back-end. 

## Nuxt.js needs a different mindset that Vue

`NuxtJS` and Vue.js handle logic very differently. The main difference is that Vue is always running on the client side, while Nuxt is not, and that can cause major problems in some cases. For example – if you want to select a DOM element right after the application is loaded, there is a possibility that the app is running on the Node.js side, and of course, there are no DOM elements in Node.js.

The same would happen when accessing a browser’s local storage. That is the main reason why Nuxt is using cookies over local storage – because they are always accessible.

With Vue, we don’t have those kinds of problems because it is always running on the client, and therefore we do not have to bother with those kind of potential problems.

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

In many small Vue applications you end up managing the structure of the code as best as you can in multiple files. The default `Nuxt.js` application structure gives you a great starting point for organizing your application in an understandable way.
You’ll first notice that `Nuxt.js` has no /src directory, these folder are in root.

[<img src="https://firebasestorage.googleapis.com/v0/b/vue-mastery.appspot.com/o/flamelink%2Fmedia%2F1578373066655_5.jpg?alt=media&token=c5fed040-8bc9-4bfe-8333-ac580c180fea" width="50%">]()

How does Nuxt render Vue pages/layouts and components?

[<img src="https://firebasestorage.googleapis.com/v0/b/vue-mastery.appspot.com/o/flamelink%2Fmedia%2F1578373061939_3.jpg?alt=media&token=2475f5b7-591f-46b9-9087-1aea19903af5" width="50%">]()

Each of these folders will contain component .vue files, and they each start out with a single default generated file, which together showed us the page we saw when we launched the development server.

[<img src="https://firebasestorage.googleapis.com/v0/b/vue-mastery.appspot.com/o/flamelink%2Fmedia%2F1578373064141_4.jpg?alt=media&token=40f2e214-094f-4140-91aa-e35ac64a508f" width="50%">]()

## SPA versus Universal Mode

### Typical Vue SPA

[<img src="https://firebasestorage.googleapis.com/v0/b/vue-mastery.appspot.com/o/flamelink%2Fmedia%2F1578373459127_0.jpg?alt=media&token=86e8ecca-a0ae-494c-bf7f-a97c09b36a70" width="50%">]()

### Universal Mode

`Universal Mode`, which means that when the application is initially loaded, it will render the page requested on the server-side first, before sending over the initial HTML.

[<img src="https://firebasestorage.googleapis.com/v0/b/vue-mastery.appspot.com/o/flamelink%2Fmedia%2F1578373459128_1.jpg?alt=media&token=a64e156d-8805-44a8-b57b-b41a3a1c5c46" width="50%">]()

The new page is shown before downloading and running any JavaScript. Once JavaScript is downloaded and run Vue is started up and the page “Hydrated,” which basically means it turns into a normal `SPA (Single Page Application)`.

You can use this option to change default nuxt mode for your project using *nuxt.config.js*

For detailed explanation on how things work, check out [Nuxt.js docs](https://nuxtjs.org).

Credits to [Vue Mastery](https://www.vuemastery.com/)

# Create a Blog with Nuxt Content

The `Nuxt Content` module is a `git files based headless CMS` that provides powerful features when it comes to write blogs, documentation sites or just adding content to any regular website. It offers us many out-of-the-box features such as easy automatic markdown rendering, live preview, content hook, and beautiful code highlighting without extra tweaking. The idea of having full control of your content, not rely on any third-party platform, and dealing with just markdown syntax is merely fantastic. Less code, less setup, and more flexibility 😉. But there is a limitation. With the current version (v1.9.0), all the content within the content folder resides in the same project repository, for `$content` to be able to fetch them.

Whereas a traditional **CMS** typically combines the content and presentation layers of a website, a third-party `headless CMS` is just the content component and focuses entirely on the administrative interface for content creators, the facilitation of content workflows and collaboration, and the organization of content into taxonomies. It doesn’t concern itself with presentation layers, templates, site structure, or design, but rather stores its content in pure format and provides access to other components (e.g. delivery front ends, analytics tools, etc.) through stateless or loosely coupled APIs.

The `headless CMS` concept is one born of the demands of the digital era and a business’s need to focus on engaging customers with personalized content via multiple channels at all stages of the customer journey. As the content in a `headless CMS` is considered “pure” (because it has no presentation layer attached) just one instance of it can be used for display on any device; website, mobile, tablet, Internet of Things devices, smart watches, etc.

`Contentful` is one example of a third-party `headless CMS` platform. It is a content infrastructure platform where content can be generated, organized and allocated to any platform. Besides this, it offers the freedom to create your own content model. Final products are delivered much faster, as developers and editors work simultaneously.

The use of powerful APIs along with top-notch documentation and samples helps build prototypes faster and more easily. It was created to help professional developers create programmable content, overcoming the drawbacks of CMSes that are designed to manage page-centric websites.

Blogs are often written with `SEO keywords` in mind so that their content jumps to the top of search results. A special algorithm scans every word, title and link, as well as the reputation of the website, to deduce the search results required by the user. The blogs that fit this algorithm best are ranked higher in search results. The algorithm is frequently modified, focusing on criteria like localization, page authority and click-through rate, as well as search via voice assistants.

## Headless CMS providers

- Contentful
- Butter CMS
- Storyblok
- Magnolia
- Strapi
- Forestry