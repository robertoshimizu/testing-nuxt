<template>
  <div id="app">
    <nav-bar />
    <Nuxt />
  </div>
</template>

<script>
import NavBar from '~/components/NavBar'
export default {
  components: {
    NavBar,
  },
  head: {
    titleTemplate: '%s - Real World Events', // <-- title template
    meta: [
      {
        hid: 'description',
        name: 'description', // <-- moved this over from index.vue
        content:
          'Where you can find all the events taking place in your neighborhood',
      },
    ],
  },
}
</script>
