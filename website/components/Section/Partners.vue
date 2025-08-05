<script setup lang="ts">

</script>

<template>

      <div class="w-screen overflow-clip  bg-white   ">

        <div class="w-full ">
          <div class=" max-w-screen-4xl overflow-x-hidden mx-auto  ">
            <div class="slider-movement flex items-center  min-w-max h-full ">
                <div class="logo" >
                  <img src="assets/images/logos/riga-logo-black.webp" alt="" class="h-full object-contain">
                </div>
              <div class="logo" >
                <img src="assets/images/vkkf.jpg" alt="" class="h-full object-contain">
              </div>
              <div class="logo" >
                <img src="assets/images/eeemergin.png" alt="" class="h-full object-contain">
              </div>
              <div class="logo" >
                <img src="assets/images/balta-nakts.jpg" alt="" class="h-full object-contain">
              </div>
              <div class="logo" >
                <img src="assets/images/maza-gilde-logo.png" alt="" class="h-full object-contain">
              </div>
              <div class="logo" >
                <img src="assets/images/rsmc_logo-1.webp" alt="" class="h-full object-contain">
              </div>

              <div class="logo" >
                <img src="assets/images/logos/riga-logo-black.webp" alt="" class="h-full object-contain">
              </div>
              <div class="logo" >
                <img src="assets/images/vkkf.jpg" alt="" class="h-full object-contain">
              </div>
              <div class="logo" >
                <img src="assets/images/eeemergin.png" alt="" class="h-full object-contain">
              </div>
              <div class="logo" >
                <img src="assets/images/balta-nakts.jpg" alt="" class="h-full object-contain">
              </div>
              <div class="logo" >
                <img src="assets/images/maza-gilde-logo.png" alt="" class="h-full object-contain">
              </div>
              <div class="logo" >
                <img src="assets/images/rsmc_logo-1.webp" alt="" class="h-full object-contain">
              </div>

              <div class="logo" >
                <img src="assets/images/logos/riga-logo-black.webp" alt="" class="h-full object-contain">
              </div>
              <div class="logo" >
                <img src="assets/images/vkkf.jpg" alt="" class="h-full object-contain">
              </div>
              <div class="logo" >
                <img src="assets/images/eeemergin.png" alt="" class="h-full object-contain">
              </div>
              <div class="logo" >
                <img src="assets/images/balta-nakts.jpg" alt="" class="h-full object-contain">
              </div>
              <div class="logo" >
                <img src="assets/images/maza-gilde-logo.png" alt="" class="h-full object-contain">
              </div>
              <div class="logo" >
                <img src="assets/images/rsmc_logo-1.webp" alt="" class="h-full object-contain">
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

  }

}
@media (min-width: 768px) {

  .slider-movement{

    animation: sm 200s linear infinite 0s;
  }
  .logo{
    height: 10rem;

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