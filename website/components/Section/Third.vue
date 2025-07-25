<script setup lang="ts">

</script>

<template>

      <div class="w-full bg-white">

        <div class="w-full h-[20rem]">
          <div class="h-[20rem] max-w-screen-4xl overflow-x-hidden mx-auto">
            <div class="slider-movement flex  min-w-max h-full ">
              <div class="h-[20rem] " style="aspect-ratio: 1.6">
                <img src="assets/images/maza-gilde-orchestra.webp" alt="" class="w-full h-full object-cover">
              </div>
              <div class="h-[20rem] " style="aspect-ratio: 1.6">
                <img src="assets/images/ex-silentio.jpg" alt="" class="w-full h-full object-cover">
              </div>
              <div class="h-[20rem] " style="aspect-ratio: 1.6">
                <img src="assets/images/regence-sonore-2.jpg" alt="" class="w-full h-full object-cover">
              </div>
              <div class="h-[20rem]  " style="aspect-ratio: 1.6">
                <img src="assets/images/regence-sonore.jpg" alt="" class="w-full h-full object-cover">
              </div>
              <div class="h-[20rem] " style="aspect-ratio: 1.6">
                <img src="assets/images/regence-sonore-3.png" alt="" class="w-full h-full object-cover">
              </div>
              <div class="h-[20rem] " style="aspect-ratio: 1.6">
                <img src="assets/images/maza-gilde.jpg" alt="" class="w-full h-full object-cover">
              </div>
              <div class="h-[20rem] " style="aspect-ratio: 1.6">
                <img src="assets/images/maza-gilde-orchestra.webp" alt="" class="w-full h-full object-cover">
              </div>
              <div class="h-[20rem] " style="aspect-ratio: 1.6">
                <img src="assets/images/ex-silentio.jpg" alt="" class="w-full h-full object-cover">
              </div>
              <div class="h-[20rem] " style="aspect-ratio: 1.6">
                <img src="assets/images/regence-sonore-2.jpg" alt="" class="w-full h-full object-cover">
              </div>
            </div>
          </div>
        </div>

        <div class="w-full h-[20rem]">
          <div class="h-[20rem] max-w-screen-4xl overflow-x-hidden mx-auto">
            <div class="slider-2-movement flex  min-w-max h-full ">
              <div class="h-[20rem] " style="aspect-ratio: 1.6">
                <img src="assets/images/maza-gilde-orchestra.webp" alt="" class="w-full h-full object-cover">
              </div>
              <div class="h-[20rem] " style="aspect-ratio: 1.6">
                <img src="assets/images/ex-silentio.jpg" alt="" class="w-full h-full object-cover">
              </div>
              <div class="h-[20rem] " style="aspect-ratio: 1.6">
                <img src="assets/images/regence-sonore-2.jpg" alt="" class="w-full h-full object-cover">
              </div>
              <div class="h-[20rem]  " style="aspect-ratio: 1.6">
                <img src="assets/images/regence-sonore.jpg" alt="" class="w-full h-full object-cover">
              </div>
              <div class="h-[20rem] " style="aspect-ratio: 1.6">
                <img src="assets/images/regence-sonore-3.png" alt="" class="w-full h-full object-cover">
              </div>
              <div class="h-[20rem] " style="aspect-ratio: 1.6">
                <img src="assets/images/maza-gilde.jpg" alt="" class="w-full h-full object-cover">
              </div>
              <div class="h-[20rem] " style="aspect-ratio: 1.6">
                <img src="assets/images/maza-gilde-orchestra.webp" alt="" class="w-full h-full object-cover">
              </div>
              <div class="h-[20rem] " style="aspect-ratio: 1.6">
                <img src="assets/images/ex-silentio.jpg" alt="" class="w-full h-full object-cover">
              </div>
              <div class="h-[20rem] " style="aspect-ratio: 1.6">
                <img src="assets/images/regence-sonore-2.jpg" alt="" class="w-full h-full object-cover">
              </div>
            </div>
          </div>
        </div>

      </div>

</template>

<style scoped>
.slider-movement{
  will-change: transform;
  animation: sm 15s linear infinite 1s;
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
  will-change: transform;
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