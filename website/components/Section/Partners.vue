<script setup lang="ts">

</script>

<template>

      <div class="w-screen overflow-clip  bg-white   ">

        <div class="w-full h-[10rem]">
          <div class="h-[10rem] max-w-screen-4xl overflow-x-hidden mx-auto">
            <div class="slider-movement flex  min-w-max h-full ">
              <div v-for="i in 3" class="flex ">
                <div class="h-[10rem] " style="aspect-ratio: 1.6">
                  <img src="assets/images/logos/riga-logo-black.webp" alt="" class="w-full h-full object-cover">
                </div>
                <div class="h-[10rem] " style="aspect-ratio: 1.6">
                  <img src="assets/images/logos/riga-logo-black.webp" alt="" class="w-full h-full object-cover">
                </div>
                <div class="h-[10rem] " style="aspect-ratio: 1.6">
                  <img src="assets/images/logos/riga-logo-black.webp" alt="" class="w-full h-full object-cover">
                </div>
                <div class="h-[10rem] " style="aspect-ratio: 1.6">
                  <img src="assets/images/logos/riga-logo-black.webp" alt="" class="w-full h-full object-cover">
                </div>
                <div class="h-[10rem] " style="aspect-ratio: 1.6">
                  <img src="assets/images/logos/riga-logo-black.webp" alt="" class="w-full h-full object-cover">
                </div>
                <div class="h-[10rem] " style="aspect-ratio: 1.6">
                  <img src="assets/images/logos/riga-logo-black.webp" alt="" class="w-full h-full object-cover">
                </div>
              </div>



            </div>
          </div>
        </div>



      </div>

</template>

<style scoped>
.slider-movement{

  animation: sm 200s linear infinite 0s;
}

@keyframes sm {

  from{
    transform: translateX(0);
  }
  to{
    transform: translateX(-50%);
  }

}
.slider-2-movement{

  transform: translateX(-20%);
  animation: sm-2 35s linear infinite 1s;
}

@keyframes sm-2 {
  from{
    transform: translateX(-20%);
  }
  to{
    transform: translateX(0%);
  }

}
</style>