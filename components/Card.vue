<!-- Please remove this file from your project -->
<template>
  <div class="max-w-md p-9 rounded-3xl shadow-2xl">
    <input class="p-2" type="text" placeholder="write a question.."><br>
    <input class="p-2" type="text" placeholder="write an answer.."><br>
    <button id="submit" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
      SUBMIT
    </button>
  </div>
</template>

<style scoped>
 .btn {
    margin: 10px;
    @apply font-bold py-2 px-4 rounded;
  }
  .btn-blue {
    @apply bg-blue-500 text-white;
  }
  .btn-blue:hover {
    @apply bg-blue-700;
  }
</style>
