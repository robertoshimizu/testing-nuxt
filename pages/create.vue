<template>
  <div
    class="container mx-auto bg-blue-100 box-border h-100 w-full p-4 border-gray-400 flex space-y-10"
  >
    <h1 class="font-sans text-2xl text-gray-800 text-start justify-left">
      Create An Event
    </h1>
    <div>
      <!-- Using utilities -->
      <button
        class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded"
      >
        Button
      </button>
    </div>
  </div>
</template>
<script>
export default {
  head() {
    return {
      title: 'Create an Event',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'You can create an event in your neighborhood',
        },
      ],
    }
  },
}
</script>
