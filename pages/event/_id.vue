<template>
  <div>
    <h1>Event {{ event.title }}</h1>
  </div>
</template>
<script>
import EventService from '@/services/EventService.js'
export default {
  async asyncData({ error, params }) {
    try {
      const { data } = await EventService.getEvent(params.id)
      return {
        event: data,
      }
    } catch (e) {
      error({
        statusCode: 503,
        message: 'Unable to fetch event #' + params.id,
      })
    }
  },
  computed: {
    id() {
      return this.$route.params.id
    },
  },
  head() {
    return {
      title: this.event.title,
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'What you need to know about the event #' + this.event.title,
        },
      ],
    }
  },
}
</script>
