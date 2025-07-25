<script setup lang="ts">

</script>

<template>
<div class=" background  w-screen grid grid-cols-2 sm:grid-cols-3 xl:grid-cols-4   ">
  <div v-for="i in 12"  class="flex justify-center items-center w-full    border-transparent " style="aspect-ratio: 1.6;">
      <div class="w-full h-full m-2 sm:m-2 lg:m-2      bg-blue-950">
        <img src="assets/images/ex-silentio.jpg" alt=""
        class="w-full h-full object-cover"
        >
      </div>
  </div>
</div>
</template>

<style scoped>

.background{
  background-color: rgba(6, 38, 133, 0.5);

}
</style>