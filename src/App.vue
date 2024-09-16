<script setup>
  import MapEmbed from "./components/MapEmbedComp.vue";
  import { ref } from "vue";

  const isDialogOpen = ref(false);
</script>

<template>
  <div class="bg-indigo-950 relative">
    <!-- popup -->
    <div v-if="isDialogOpen" class="absolute inset-0 bg-black bg-opacity-50 flex justify-center items-center">
      <div class="bg-slate-900 p-4 rounded max-w-md">
        <h1 class="text-white text-2xl font-bold handwrite">How To Join?</h1>
        <p class="text-white mt-2">
          <span class="font-bold">Server IP:</span>
          <span class="font-bold text-xl"> mc.kyuiki.com </span>
        </p>
        <p class="text-amber-200">If you are using cracked version of minecraft, Please contact @kyuiki on discord.</p>
        <button @click="isDialogOpen = false" class="bg-red-500 text-white px-4 py-1 rounded mt-6">Close</button>
      </div>
    </div>
    <button
      @click="isDialogOpen = true"
      class="absolute top-2 left-1/2 -translate-x-1/2 bg-blue-500 text-white px-4 py-2 rounded-b-lg"
    >
      How To Join?
    </button>
    <MapEmbed />
  </div>
</template>

<style scoped>
  .handwrite {
    font-family: "Lato";
  }
</style>
