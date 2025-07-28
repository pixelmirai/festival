<script setup lang="js">
import {useInView} from "~/composables/useInView";
import {useUtils} from "~/composables/useUtils";
const inView = ref(false)
const images = ref(null)
const imagesInView = ref(false)
const section = ref(null)
const text1 = "Rīgas Vēsturiskās mūzikas un dejas festivāls 2025 ir starptautisks kultūras notikums, kas notiks no 6. septembra līdz 11. oktobrim dažādās Rīgas koncertvietās."
const text2 = " Festivāls piedāvā bagātīgu programmu ar senās mūzikas koncertiem, koncertlekcijām un garīgās mūzikas notikumiem, pulcējot augsta līmeņa māksliniekus no Latvijas un ārzemēm. Tajā uzstāsies tādi atzīti kolektīvi kā Collegium Musicum Riga, Neymann Ensemble, Regence Sonore un Coloquio 6, kā arī ievērojami solisti, piemēram, Ēriks Bosgrāfs, Elīna Šimkus un Mauro Pinciaroli."
const text3 = "Rīgas Vēsturiskās mūzikas un dejas festivāls ir kā mājas, kurā gan skatītāji un klausītāji, gan paši mūziķi un mākslinieki ar īpašu prieku atgriežas, lai atgūtu harmoniju, smeltos enerģiju, kaut uz brīdi iejustos augsti izglītoto un smalkjūtīgo baroka laika galminieku ādā, un, kas īpaši būtiski – pārsteigumā secinātu, cik patiesībā daudz mēs vēl varam atklāt. Visi festivāla koncerti tiek atskaņoti tikai un vienīgi ar vēsturisko mūzikas instrumentu oriģināliem vai to kopijām, dziedātāju balsis pārvalda baroka laika ornamentus un retoriskos smalkumus, pilnībā aizslaukot māņu mītus par seno mūziku kā kaut ko vecmodīgu. Tieši pretēji – pateicoties Rīgas Vēsturiskās mūzikas un dejas festivāla norisēm, Rīga un Latvija ir kļuvusi par vienu no nozīmīgākajiem senās mūzikas centriem Eiropā.Festivāls piedāvā klausītājiem ceļojumu laikā, iepazīstinot ar Eiropas 17.–18. gadsimta mūziku un vēsturiskajiem instrumentiem. Programmā iekļauti gan klasiskās baroka mūzikas šedevri, gan arī mazāk zināmi, bet muzikāli vērtīgi darbi."

const utils = useUtils();
const visibleHeightRatio = ref(0)
const shadowSize = ref(0)

const rightShadow = ref(0);
const bottomShadow = ref(0);

onMounted(()=>{
  if(section.value){
    useInView(section.value,()=>{

      inView.value = true;
    },0.2)
  }
  if(images.value){
    useInView(images.value,()=>{
      imagesInView.value = true;
      console.log("in")
    },0)
  }



})

function calculateShadow(vhr){
  return 60 - (55 * vhr);
}

function calculateRightShadow(vhr){
  return 60 - (55 * vhr);
}


function calculateBottomShadow(vhr){
  return 100 - (93 * vhr);
}


</script>

<template>
  <div   ref="section"  class=" max-w-screen overflow-x-clip bg-white"  >
    <div class="max-w-screen-2xl mx-auto">
      <div class=" flex flex-col-reverse md:flex-row py-16  max-w-screen-2xl mx-auto ">

        <div  class="relative flex justify-center items-center w-full  md:w-1/2 min-w-[360px] ">
         <FallingImages class="z-10"/>
        </div>
        <div class="flex justify-center items-center w-full  md:w-1/2 min-w-[360px] ">

          <div class="big-text  p-8  ">
            <div class="overflow-clip pb-2 pr-2  ">
              <div
                  :class="{'description-text-shadow' : inView}"
                  class="flex flex-col pb-16 pr-16   gap-12  ">
                <p class=" text-3xl  md:text-5xl font-extralight text-center ">
                  {{text1}}

                </p>
              </div>
            </div>
          </div>

        </div>
      </div>



    </div>



  </div>


</template>

<style scoped>
.description-text-shadow{
  opacity: 1;
  box-shadow: black -5rem 2px 0,
  black 2px -2rem 0;
  animation: description-text-shadow-fade 3s ;

}
@keyframes description-text-shadow-fade {
  from{
    opacity: 0;
    box-shadow: black -30rem 2px 0,
    black 2px -30rem 0;
  }
  to {
    opacity: 1;
    box-shadow: black -5rem 2px 0,
    black 2px -2rem 0;
  }
}


.image-1 {
  transform: translateX(-100rem) translateY(-100rem) rotateZ(0deg);
  animation: insert-image-1 1s linear 0s forwards;
}

.image-2 {
  transform: translateX(-100rem) translateY(-100rem) rotateZ(0deg);
  animation: insert-image-2 1s linear 1s forwards;
}

.image-3 {
  transform: translateX(-100rem) translateY(-100rem) rotateZ(0deg);
  animation: insert-image-3 1s linear 2s forwards;
}

.image-4 {
  transform: translateX(-100rem) translateY(-100rem) rotateZ(0deg);
  animation: insert-image-4 1s linear 3s forwards;
}

.image-5 {
  transform: translateX(-100rem) translateY(-100rem) rotateZ(0deg);
  animation: insert-image-5 1s linear 4s forwards;
}


@keyframes insert-image-1 {
  from {
    transform: translateX(-100rem) translateY(-100rem) rotateZ(0deg);
  }
  to {
    transform: translateX(0) translateY(0) rotateZ(0deg);
  }
}

@keyframes insert-image-2 {
  from {
    transform: translateX(-100rem) translateY(-100rem) rotateZ(0deg);
  }
  to {
    transform: translateX(-1rem) translateY(-1rem) rotateZ(-2deg);
  }
}

@keyframes insert-image-3 {
  from {
    transform: translateX(-100rem) translateY(-100rem) rotateZ(0deg);
  }
  to {
    transform: translateX(-2rem) translateY(-2rem) rotateZ(-20deg);
  }
}

@keyframes insert-image-4 {
  from {
    transform: translateX(-100rem) translateY(-100rem) rotateZ(0deg);
  }
  to {
    transform: translateX(-5rem) translateY(2rem) rotateZ(60deg);
  }
}

@keyframes insert-image-5 {
  from {
    transform: translateX(-100rem) translateY(-100rem) rotateZ(0deg);
  }
  to {
    transform: translateX(2rem) translateY(4rem) rotateZ(10deg);
  }
}



</style>