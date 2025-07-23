<script setup lang="js">

</script>

<template>
<div class="relative h-[64rem] w-screen  overflow-clip bg-[rgb(0,0,0,0.9)]">
    <div class=" w-full h-full flex justify-center items-center">

      <div class="outer h-[12rem] w-full translate-x-44  ">
        <div class="inner relative h-[12rem] w-full-   ">

          <div class="absolute ">
            <div class="absolute h-full flex  gap-4 flex-nowrap min-w-max slider-movement ">
              <div v-for="i in 10" class=" rounded-lg border-2 border-white  overflow-clip h-[12rem] aspect-[1.5]">
                <img src="assets/images/maza-gilde-2.jpg" alt="" class="w-full h-full object-cover">
              </div>
            </div>
          </div>

        </div>
      </div>

    </div>
</div>
</template>

<style scoped>

.outer {
  perspective: 800px;
}

.inner {

  transform: rotateX(15deg) rotateY(50deg) rotateZ(10deg);
}

slider-1-container{
  perspective: 1000px;
}
.slider-1{

  transform: rotateZ(20deg) rotateX(20deg)  ;
}

.slider-movement{
  animation: sm 1200s  forwards;

}
@keyframes sm {
  from{
    transform: translateX(0);
  }
  to{
    transform: translateX(-100%);
  }

}

</style>