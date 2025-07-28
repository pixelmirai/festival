<script setup lang="js">




onMounted(()=>{


})
</script>

<template>
<div class="relative w-[100vw] h-[48rem] border border-black  bg-white overflow-clip    ">
  <div class="absolute w-full h-full flex justify-center items-center">
    <div class="absolute w-full h-full ">
      <img src="assets/images/rigagpt-1.png" alt="" class="w-full max-w-screen-xl mx-auto object-contain ">
    </div>
      <div class="absolute w-[360px] h-[40rem] border-4 border-black">
          <div class="w-full  h-full">
            <img src="assets/images/maza-gilde.jpg" alt="" class="w-full h-full object-cover  ">
          </div>
      </div>
    <div class="absolute w-[360px] h-[40rem] border-4 border-black">
      <div class="w-1/2 h-full">
        <img src="assets/images/violin-splash.png" alt="" class="w-full h-full object-cover -translate-x-6 -translate-y-6 ">
      </div>
    </div>
  </div>
  <div class="absolute flex justify-center items-center w-full h-full object-cover">
        <div class="perspective   relative ">

            <div class=" container relative overflow-y-clip  w-[360px] grid grid-cols-2 gap-2   ">

                <div v-for="i in 8 " class="w-full t  flex justify-center items-center aspect-square ">
                  <img src="assets/images/orchestra-church.webp" alt="" class="">
                </div>
            </div>
        </div>

  </div>



</div>
</template>

<style scoped>
.perspective{
  perspective: 800px;
}

@media (min-width: 748px) {

  .container{
    transform: rotateZ(50deg) rotateX(40deg)  rotateY(-50deg) ;
  }

}

</style>