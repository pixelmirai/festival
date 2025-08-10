<script setup lang="js">
const logos = ref([""])

const IMG_URL = "https://rvmdfcontent.wordpress.com/wp-content/uploads/2025/08/";

const partners = {
  baltaNakts: IMG_URL + 'partners-balta-nakts.webp',
  bilesuParadize: IMG_URL + 'partners-bilesu-paradize.webp',
  bolderajasElb: IMG_URL + 'partners-bolderajas-elb.webp',
  collegium: IMG_URL + 'partners-collegium.webp',
  eu: IMG_URL + 'partners-eu.webp',
  kulturasMinistrija: IMG_URL + 'partners-kulturas-ministrija.webp',
  mazaGilde: IMG_URL + 'partners-maza-gilde.webp',
  rembatesSokola: IMG_URL + 'partners-rembates-sokola.webp',
  riga: IMG_URL + 'partners-riga.webp',
  rsmc: IMG_URL + 'partners-rsmc.webp',
  se: IMG_URL + 'partners-se.webp',
  vkkf: IMG_URL + 'partners-vkkf.webp',
};


onMounted(()=>{

})

</script>

<template>

      <div class="w-screen overflow-clip  bg-white   ">

        <div class="w-full ">
          <div class=" max-w-screen-4xl overflow-x-hidden mx-auto  ">
            <div class="slider-movement flex   min-w-max h-full ">

              <div v-for="i in 4" class="flex gap-2  py-8 sm:py-0  items-center ">
                <div class="logo">
                  <img src="assets/images/partners/partners-riga.webp" alt="Rīgas dome" class="h-full object-contain">
                </div>
                <div class="logo">
                  <img src="assets/images/partners/partners-maza-gilde.webp" alt="Mazā Ģilde" class="h-full object-contain">
                </div>
                <div class="logo">
                  <img src="assets/images/partners/partners-kulturas-ministrija.webp" alt="Kultūras ministrija" class="h-full object-contain">
                </div>
                <div class="logo">
                  <img src="assets/images/partners/partners-vkkf.webp" alt="VKKF" class="h-full object-contain">
                </div>
                <div class="logo">
                  <img src="assets/images/partners/partners-balta-nakts.webp" alt="Baltā nakts" class="h-full object-contain">
                </div>
                <div class="logo">
                  <img src="assets/images/partners/partners-rembates-sokolade.webp" alt="Rembates šokolāde" class="h-full object-contain">
                </div>
                <div class="logo">
                  <img src="assets/images/partners/partners-bilesu-paradize.webp" alt="Biļešu paradīze" class="h-full object-contain">
                </div>
                <div class="logo">
                  <img src="assets/images/partners/partners-se.webp" alt="SE" class="h-full object-contain">
                </div>
                <div class="logo">
                  <img src="assets/images/partners/partners-eu.webp" alt="EU" class="h-full object-contain">
                </div>
                <div class="logo">
                  <img src="assets/images/partners/partners-collegium.webp" alt="Collegium Musicum Riga" class="h-full object-contain">
                </div>
                <div class="logo">
                  <img src="assets/images/partners/partners-rsmc.webp" alt="RSMC" class="h-full object-contain">
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