<script setup lang="js">
const logos = ref([""])

onMounted(()=>{

})

</script>

<template>

      <div class="w-screen overflow-clip  bg-white   ">

        <div class="w-full ">
          <div class=" max-w-screen-4xl overflow-x-hidden mx-auto  ">
            <div class="slider-movement flex   min-w-max h-full ">

              <div v-for="i in 4" class="flex gap-2  py-8 sm:py-0  items-center ">
                <div class="logo" >
                  <img src="assets/images/partners/partners-riga.jpg" alt="" class="h-full object-contain">
                </div>
                <div class="logo" >
                  <img src="assets/images/partners/partners-maza-gilde.jpg" alt="" class="h-full object-contain">
                </div>
                <div class="logo" >
                  <img src="assets/images/partners/partners-kulturas-ministrija.jpg" alt="" class="h-full object-contain">
                </div>
                <div class="logo" >
                  <img src="assets/images/partners/partners-vkkf.jpg" alt="" class="h-full object-contain">
                </div>
                <div class="logo" >
                  <img src="assets/images/partners/partners-balta-nakts.jpg" alt="" class="h-full object-contain">
                </div>
                <div class="logo" >
                  <img src="assets/images/partners/partners-rembates-sokolade.jpg" alt="" class="h-full object-contain">
                </div>
                <div class="logo" >
                  <img src="assets/images/partners/partners-bilesu-paradize.jpg" alt="" class="h-full object-contain">
                </div>
                <div class="logo" >
                  <img src="assets/images/partners/partners-se.jpg" alt="" class="h-full object-contain">
                </div>
                <div class="logo" >
                  <img src="assets/images/partners/partners-eu.png" alt="" class="h-full object-contain">
                </div>
                <div class="logo" >
                  <img src="assets/images/partners/partners-collegium.jpg" alt="" class="h-full object-contain">
                </div>
                <div class="logo" >
                  <img src="assets/images/partners/partners-rsmc.jpg" alt="" class="h-full object-contain">
                </div>

              </div>






            </div>


          </div>
        </div>



      </div>

</template>

<style scoped>

@media (max-width: 767px) {

  .slider-movement{

    animation: sm 50s linear infinite 0s;
  }
  .logo{
    height: 5rem;
    aspect-ratio: 1;
    padding: 0.2rem;
    border: solid white;
  }

}
@media (min-width: 768px) {

  .slider-movement{

    animation: sm 150s linear infinite 0s;
  }
  .logo{
    height: 8rem;
    aspect-ratio: 1;
    padding: 0.8rem;
    border: solid white;


  }

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