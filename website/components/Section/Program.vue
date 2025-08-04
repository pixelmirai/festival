<script setup lang="js">
import { useRouter } from "vue-router";

const mazaGilde = "https://maps.app.goo.gl/1VRCZxZ65KwyMzXXA";
const collegiumZale = "https://maps.app.goo.gl/qxiCgmYymshP3jz67";
const magdalena = "https://maps.app.goo.gl/sbecYuJLmT3JSpFn6";
const bolderaja = "https://maps.app.goo.gl/2hNPemBN7wiASMgN6";

const router = useRouter();

const program = [
  {

  }
];

const atklasanaOpen = ref(false);
const regenceSonoreOpen = ref(false);
const inExiliumOpen = ref(false);
const neymannOpen = ref(false);
const stastiMilestibaOpen = ref(false);
const mocartsOpen = ref(false);
const saulrietsOpen = ref(false);
const italijasValdzinajumsOpen = ref(false);
const revalersOpen = ref(false);
const noslegumsOpen = ref(false);
</script>

<template>
  <div class="bg-white pb-8">
    <div class="max-w-screen-2xl mx-auto">

      <div>
        <h2 class="text-center py-32 uppercase text-5xl md:text-6xl lg:text-7xl font-serif">
          Festivāla programma
        </h2>
      </div>

      <div class="programm-list mx-auto max-w-screen-2xl">


        <div class="program-item mx-4">
          <div>
            <p class="font-bold text-2xl text-gray-600 uppercase">
              <span>6. septembris </span><span>18:00 </span> <span class="font-extralight">Sestdiena</span>
            </p>
          </div>

          <div class="flex flex-col py-4 gap-2 border-b border-gray-200">
            <h2 class="text-3xl font-serif">
              Festivāla atkāšanas koncerts Baltās Nakts ietvaros
            </h2>
            <h3 class="text-xl font-bold italic">
              Četri pretendenti Leipcigā: Bahs, Tēlemanis, Graupners un Fašs - virtuozā vācu baroka mūzika
            </h3>
          </div>

          <div class="pt-4">
            Baroka orķestris <strong>Collegium Musicum Riga</strong>,
            <strong>Ēriks Bosgrafs</strong> (Nīderlande) un orķestra solisti.
          </div>

          <div>
            <div class="flex justify-center py-4">
              <a :href="mazaGilde" target="_blank" rel="noopener noreferrer">
                <p class="hover:underline text-xl font-semibold">
                  RKTMC <span class="italic pr-2">Mazā Ģilde</span>

                </p>
                <p class="text-center py-2  ">
                  <span class="pr-2 "> Amatu iela 5, Rīga</span>
                  <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="currentColor"
                       class="bi bi-geo-alt-fill inline -translate-y-1" viewBox="0 0 16 16">
                    <path
                        d="M8 16s6-5.686 6-10A6 6 0 0 0 2 6c0 4.314 6 10 6 10m0-7a3 3 0 1 1 0-6 3 3 0 0 1 0 6" />
                  </svg>
                </p>
              </a>
            </div>

            <div class="description py-8 overflow-clip"
                 :class="atklasanaOpen ? '' : 'hidden'">
              <div class="w-full flex justify-center items-center pb-8">
                <div class="w-full">
                  <img src="assets/images/regence-sonore.jpg" alt=""
                       class="w-full h-full object-cover" />
                </div>
              </div>
              <article></article>
            </div>

            <div class="buttons flex">
              <p class="flex justify-start items-end w-1/2">
                Ieeja ar bezmaksas ielūgumiem
              </p>
              <div class="flex justify-end items-center w-1/2">
                <button
                    @click="atklasanaOpen = !atklasanaOpen"
                    class="bg-black text-white w-[6rem] hover:bg-white hover:text-black border-2 border-black cursor-pointer"
                    style="aspect-ratio: 1.6">
                  {{ atklasanaOpen ? 'Aizvērt' : 'Lasīt' }}
                </button>
              </div>
            </div>
          </div>
        </div>

        <div class="w-full my-16 border-t border-black mx-4"></div>

        <div class="program-item mx-4">
          <div>
            <p class="font-bold text-2xl text-gray-600 uppercase">
              <span>13. septembris </span><span>18:00 </span> <span class="font-extralight">Sestdiena</span>
            </p>
          </div>

          <div class="flex flex-col py-4 gap-2 border-b border-gray-200">
            <h2 class="text-3xl font-serif">
              Ansamblis <span class="italic">Regence Sonore</span> (Polija)
            </h2>
          </div>

          <div>
            <div class="flex justify-center py-4">
              <a :href="collegiumZale" target="_blank" rel="noopener noreferrer">
                <p class="hover:underline text-xl font-semibold">
                  Koncertzāle: <span class="italic pr-2">Collegium Musicm Riga</span>
                </p>
                <p class="text-center py-2">
                  <span class="pr-2">Vaļņu iela 9-3, Rīga</span>
                  <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="currentColor"
                       class="bi bi-geo-alt-fill inline -translate-y-1" viewBox="0 0 16 16">
                    <path
                        d="M8 16s6-5.686 6-10A6 6 0 0 0 2 6c0 4.314 6 10 6 10m0-7a3 3 0 1 1 0-6 3 3 0 0 1 0 6" />
                  </svg>
                </p>
              </a>
            </div>


            <div class="description py-8 overflow-clip"
                 :class="regenceSonoreOpen ? '' : 'hidden'">
              <div class="w-full flex justify-center items-center pb-8">
                <div class="w-full">
                  <img src="assets/images/regence-sonore.jpg" alt=""
                       class="w-full h-full object-cover" />
                </div>
              </div>
              <article>
                Régence sonore – izcils poļu mākslinieču dibināts senās mūzikas ansamblis – apvieno augstākos Eiropas senās mūzikas izglītības sasniegumus ar spilgtu māksliniecisko identitāti un mērķtiecīgu skatu nākotnē. Trio sastāvā muzicē Weronika Zimnoch (vēsturiskā vijole), Krystyna Wiśniewska (vēsturiskais čells) un Weronika Paine (klavesīns), radot bagātīgu un niansētu skanējumu.

                2024. gadā ansamblis piedzīvoja savu konkursa debiju prestižajā Göttingen Händel competition, kur starptautiskā žūrija tam piešķīra divas no piecām galvenajām balvām. Šis sasniegums vainagojās arī ar nomināciju Polijas mūzikas balvai “Gada atklājums” (Coryphaeus of Music in Poland).

                Ansambļa koncerts Latvijā notiek S-Eeemerging rezidences ietvaros, ar Eiropas Savienības programmas "Radošā Eiropa" atbalstu.
                ​
              </article>
            </div>

            <div class="flex ">
              <div class="flex justify-start items-end w-1/2">
                <a href="https://www.bilesuparadize.lv/lv/event/154875" target="_blank" rel="noopener noreferrer">
                  <button
                      class="bg-[#5B8930] border-2 border-[#5B8930] text-white w-[6rem] hover:bg-white hover:text-[#5B8930] cursor-pointer"
                      style="aspect-ratio: 1.6">
                    Biļetes
                  </button>
                </a>
              </div>
              <div class="flex justify-end items-center w-1/2">
                <button
                    @click="regenceSonoreOpen = !regenceSonoreOpen"
                    class="bg-black text-white w-[6rem] hover:bg-white hover:text-black border-2 border-black cursor-pointer"
                    style="aspect-ratio: 1.6">
                  {{ regenceSonoreOpen ? 'Aizvērt' : 'Lasīt' }}
                </button>
              </div>
            </div>
          </div>
        </div>

        <div class="w-full my-16 border-t border-black mx-4"></div>

        <div class="program-item mx-4">
          <div>
            <p class="font-bold text-2xl text-gray-600 uppercase">
              <span>16. septembris </span><span>19:00 </span> <span class="font-extralight">Otrdiena</span>
            </p>
          </div>

          <div class="flex flex-col py-4 gap-2 border-b border-gray-200">
            <h2 class="text-3xl font-serif">
              Koncerts-lekcija <span class="italic">In Exilium</span>, viduslaiku mūzikas ansamblis
              <span class="italic">Ex Silentio</span> (Grieķija)
            </h2>
          </div>

          <div>
            <div class="flex justify-center py-4">
              <a :href="collegiumZale" target="_blank" rel="noopener noreferrer">
                <p class="hover:underline text-xl font-semibold">
                  Koncertzāle: <span class="italic pr-2">Collegium Musicm Riga</span>
                </p>
                <p class="text-center py-2">
                  <span class="pr-2">Vaļņu iela 9-3, Rīga</span>
                  <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="currentColor"
                       class="bi bi-geo-alt-fill inline -translate-y-1" viewBox="0 0 16 16">
                    <path
                        d="M8 16s6-5.686 6-10A6 6 0 0 0 2 6c0 4.314 6 10 6 10m0-7a3 3 0 1 1 0-6 3 3 0 0 1 0 6" />
                  </svg>
                </p>
              </a>
            </div>

            <div class="description py-8 overflow-clip"
                 :class="inExiliumOpen ? '' : 'hidden'">
              <div class="w-full flex justify-center items-center pb-8">
                <div class="w-full">
                  <img src="assets/images/regence-sonore.jpg" alt=""
                       class="w-full h-full object-cover" />
                </div>
              </div>
              <article>
                <strong>
                  Ceļojums viduslaiku mūzikā – lekcija-koncerts ar Dr. Dimitri Kountouras un Irini Bilini-Moraiti
                </strong>

                Aizraujošā lekcija-koncertā klausītāji aicināti doties muzikālā ceļojumā cauri viduslaiku pasaulei, kur saplūst garīgā un laicīgā mūzika, improvizācija un senie skaņu ideāli. Iepazīstot viduslaiku flautas, blokflautas, stīgu instrumentus, kā arī dziedāšanas un spēles tehnikas, mākslinieki atklāj viduslaiku mūzikas interpretācijas daudzslāņainību.

                Programmā skan darbi no trubadūru repertuāra, Guillaume de Machaut, kā arī Austrumu Vidusjūras mūzikas tradīcijām, kuras vieno modālā domāšana un improvizācija.

                Dr. Dimitris Kountouras – viens no redzamākajiem Grieķijas senās mūzikas interpretiem – ir Atēnu Konservatorijas un Jonijas Universitātes profesors, kā arī ansambļa Ex Silentio mākslinieciskais vadītājs.

                Irini Bilini-Moraiti specializējas senajā dziedāšanā un viduslaiku stīgu instrumentos, sniedzot autentisku priekšstatu par viduslaiku skaņu pasauli.

              </article>
            </div>

            <div class="flex">
              <div class="flex justify-start items-end w-1/2">
                <a href="https://www.bilesuparadize.lv/lv/event/154884" target="_blank" rel="noopener noreferrer">
                  <button
                      class="bg-[#5B8930] border-2 border-[#5B8930] text-white w-[6rem] hover:bg-white hover:text-[#5B8930] cursor-pointer"
                      style="aspect-ratio: 1.6">
                    Biļetes
                  </button>
                </a>
              </div>
              <div class="flex justify-end items-center w-1/2">
                <button
                    @click="inExiliumOpen = !inExiliumOpen"
                    class="bg-black text-white w-[6rem] hover:bg-white hover:text-black border-2 border-black cursor-pointer"
                    style="aspect-ratio: 1.6">
                  {{ inExiliumOpen ? 'Aizvērt' : 'Lasīt' }}
                </button>
              </div>
            </div>
          </div>
        </div>

        <div class="w-full my-16 border-t border-black mx-4"></div>

        <div class="program-item mx-4">
          <div>
            <p class="font-bold text-2xl text-gray-600 uppercase">
              <span>20. septembris </span><span>20:00 </span> <span class="font-extralight">Sestdiena</span>
            </p>
          </div>

          <div class="flex flex-col py-4 gap-2 border-b border-gray-200">
            <h2 class="text-3xl font-serif">
              <span>Neymann Ensemble</span> (Latvija, Austrija, Itālija)
            </h2>
            <h3 class="text-xl font-bold italic">
              Amorose ai rai del sole (Venēcijas mūzika)
            </h3>
          </div>

          <div>
            <div class="flex justify-center py-4">
              <a :href="magdalena" target="_blank" rel="noopener noreferrer">
                <p class="hover:underline text-xl font-semibold">
                  <span class="italic pr-2">Rīgas Svētās Marijas Magdalēnas baznīca</span>
                </p>
                <p class="text-center py-2">
                  <span class="pr-2">Klostera iela 2, Rīga</span>
                  <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="currentColor"
                       class="bi bi-geo-alt-fill inline -translate-y-1" viewBox="0 0 16 16">
                    <path
                        d="M8 16s6-5.686 6-10A6 6 0 0 0 2 6c0 4.314 6 10 6 10m0-7a3 3 0 1 1 0-6 3 3 0 0 1 0 6" />
                  </svg>
                </p>
              </a>
            </div>


            <div class="description py-8 overflow-clip"
                 :class="neymannOpen ? '' : 'hidden'">
              <div class="w-full flex justify-center items-center pb-8">
                <div class="w-full">
                  <img src="assets/images/regence-sonore.jpg" alt=""
                       class="w-full h-full object-cover" />
                </div>
              </div>
              <article>
                <strong>
                  NEYMANN ENSEMBLE atgriešanās uz Latvijas senās mūzikas skatuves
                </strong>
                Koncertprogramma “Amorosa ai rai del sole” klausītājus vedīs uz Veneto reģionu Itālijā, kuru labāk pazīstam kā Venēcijas valsti 18.gadsimtā. Tieši Veneto ir dzimtene daudziem vēl mūsdienās labi pazīstamiem baroka laika komponistiem, kā piemēram, Antonio Vivaldi vai Klaudio Monteverdi. Virtuozo ansambļa mūziķu izpildījumā izskanēs opusi no A.Vivaldi, T.Albinoni, Dž.Dž.Kapsbergera un B.Marčello opusiem.

                Starptautiskā senās mūzikas asambļa “Neymann Ensemble” pirmsākumi ir meklējami 2014. gadā, kad trīs no ansambļa mūziķiem satikās Vīnes Mūzikas un mākslas privātajā universitātē, kur katrs no viņiem bija nonācis, lai iegūtu vai papildinātu zināšanas senajā mūzikā. Neymann Ensemble ir muzicējis gan mazākā, gan lielākā mūziķu sastāvā. Šobrīd ansamblī muzicē Maija Kania (vijole), Elīna Vidriķe (dulčiana, baroka fagots, blokflauta), Mauro Pičaroli /Mauro Piciaroli/ IT (lauta, teorba) un Ernests Neimanis / AT (klavesīns). Šāds instrumentu sastāvs ansamblī nav pārāk bieži izplatīts, tāpēc mūziķiem ir izaicinājums atrast, izveidot un pielāgot repertuāru tā, lai to varētu atskaņot publikai baudāmā galarezultātā. Šāda atskaņojuma prakse bija ļoti izplatīta 17. un 18. gadsimtā.
              </article>
            </div>

            <div class="flex">
              <div class="flex justify-start items-end w-1/2">
                <a href="https://www.bilesuparadize.lv/lv/event/154881" target="_blank" rel="noopener noreferrer">
                  <button
                      class="bg-[#5B8930] border-2 border-[#5B8930] text-white w-[6rem] hover:bg-white hover:text-[#5B8930] cursor-pointer"
                      style="aspect-ratio: 1.6">
                    Bezmaksas IELŪGUMS
                  </button>
                </a>
              </div>
              <div class="flex justify-end items-center w-1/2">
                <button
                    @click="neymannOpen = !neymannOpen"
                    class="bg-black text-white w-[6rem] hover:bg-white hover:text-black border-2 border-black cursor-pointer"
                    style="aspect-ratio: 1.6">
                  {{ neymannOpen ? 'Aizvērt' : 'Lasīt' }}
                </button>
              </div>
            </div>
          </div>
        </div>

        <div class="w-full my-16 border-t border-black mx-4"></div>

        <div class="program-item mx-4">
          <div>
            <p class="font-bold text-2xl text-gray-600 uppercase">
              <span>22. septembris </span><span>19:00 </span> <span class="font-extralight">Pirmdiena</span>
            </p>
          </div>

          <div class="flex flex-col py-4 gap-2 border-b border-gray-200">
            <h2 class="text-3xl font-serif">
              Koncerts <span class="italic">Stāsti (man) par mīlestību</span>
            </h2>
          </div>

          <div class="pt-4">
            <strong>Anete Viļuma</strong> (soprāns),
            <strong>Mauro Pinciaroli</strong> (Lauta, Itālija)
          </div>

          <div>
            <div class="flex justify-center py-4">
              <a :href="collegiumZale" target="_blank" rel="noopener noreferrer">
                <p class="hover:underline text-xl font-semibold">
                  Koncertzāle: <span class="italic pr-2">Collegium Musicm Riga</span>
                </p>
                <p class="text-center py-2">
                  <span class="pr-2"> Vaļņu iela 9-3, Rīga</span>
                  <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="currentColor"
                       class="bi bi-geo-alt-fill inline -translate-y-1" viewBox="0 0 16 16">
                    <path
                        d="M8 16s6-5.686 6-10A6 6 0 0 0 2 6c0 4.314 6 10 6 10m0-7a3 3 0 1 1 0-6 3 3 0 0 1 0 6" />
                  </svg>
                </p>
              </a>
            </div>


            <div class="description py-8 overflow-clip"
                 :class="stastiMilestibaOpen ? '' : 'hidden'">
              <div class="w-full flex justify-center items-center pb-8">
                <div class="w-full">
                  <img src="assets/images/regence-sonore.jpg" alt=""
                       class="w-full h-full object-cover" />
                </div>
              </div>
              <article>
                STĀSTI (MAN) PAR MĪLESTĪBU būs ceļojums mūzikas un dzejas pasaulē, iepazīstot ne tikai dažādu angļu komponistu daiļradi, bet arī renesanses laika angļu dzejnieku rindas par mīlestību.

                Koncertprogrammā satiksies unikāls sastāvs -  šarmantā un valdzinošā dziedātāja Anete VIĻUMA (soprāns)

                Latvijas klausītājiem jau pazīstamais itāļu lautists Mauro PINCIAROLI, kurš nekad un nevienu neatstāj vienaldzīgu ar savu izsmalcināto un meistarīgo lautas spēli.

              </article>
            </div>

            <div class="flex">
              <div class="flex justify-start items-end w-1/2">
                <a href="https://www.bilesuparadize.lv/lv/event/154883" target="_blank" rel="noopener noreferrer">
                  <button
                      class="bg-[#5B8930] border-2 border-[#5B8930] text-white w-[6rem] hover:bg-white hover:text-[#5B8930] cursor-pointer"
                      style="aspect-ratio: 1.6">
                    Bezmaksas IELŪGUMS
                  </button>
                </a>
              </div>
              <div class="flex justify-end items-center w-1/2">
                <button
                    @click="stastiMilestibaOpen = !stastiMilestibaOpen"
                    class="bg-black text-white w-[6rem] hover:bg-white hover:text-black border-2 border-black cursor-pointer"
                    style="aspect-ratio: 1.6">
                  {{ stastiMilestibaOpen ? 'Aizvērt' : 'Lasīt' }}
                </button>
              </div>
            </div>
          </div>
        </div>

        <div class="w-full my-16 border-t border-black mx-4"></div>


        <div class="program-item mx-4">
          <div>
            <p class="font-bold text-2xl text-gray-600 uppercase">
              <span>25. septembris </span><span>19:00 </span> <span class="font-extralight">Ceturtdiena</span>
            </p>
          </div>

          <div class="flex flex-col py-4 gap-2 border-b border-gray-200">
            <h2 class="text-3xl font-serif">
              Koncertlekcija <span class="italic">Mocarts un sievietes viņa dzīvē (un mākslā)</span>
            </h2>
          </div>

          <div class="pt-4">
            <strong>Māris Kupčs</strong> (lektors, klavesīns),
            <strong>Monta Martinsone</strong> (soprāns)
          </div>

          <div>
            <div class="flex justify-center py-4">
              <a :href="collegiumZale" target="_blank" rel="noopener noreferrer">
                <p class="hover:underline text-xl font-semibold">
                  Koncertzāle: <span class="italic pr-2">Collegium Musicm Riga</span>
                </p>
                <p class="text-center py-2">
                  <span class="pr-2">Vaļņu iela 9-3, Rīga</span>
                  <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="currentColor"
                       class="bi bi-geo-alt-fill inline -translate-y-1" viewBox="0 0 16 16">
                    <path
                        d="M8 16s6-5.686 6-10A6 6 0 0 0 2 6c0 4.314 6 10 6 10m0-7a3 3 0 1 1 0-6 3 3 0 0 1 0 6" />
                  </svg>
                </p>
              </a>
            </div>


            <div class="description py-8 overflow-clip"
                 :class="mocartsOpen ? '' : 'hidden'">
              <div class="w-full flex justify-center items-center pb-8">
                <div class="w-full">
                  <img src="assets/images/regence-sonore.jpg" alt=""
                       class="w-full h-full object-cover" />
                </div>
              </div>
              <article>
                Volfgangs Amadejs Mocarts – neviennozīmīga personība, viennozīmīgs ģēnijs!

                Aicinām uz aizraujošu muzikālu tikšanos, kurā skanēs sarunas un mūzika, atklājot, kā sievietes ietekmējušas Mocarta dzīvi un daiļradi – no mūzām un kolēģēm līdz viņa ģimenes sievietēm.

                Mūzikas vēsturnieks un klavesīnspēles meistars Māris Kupčs dalīsies stāstos par Mocarta laikmeta kultūras fonu, savukārt soprāns Monta Martinsone, kuras balss apvieno spožumu un izsmalcinātību, iedzīvinās Mocarta mūziku ar emocionālu un stilistiski autentisku izpildījumu.

                Šis vakars būs inteliģenta humora, spilgtu faktu un neaizmirstamas mūzikas piepildīts – neaizmirstiet rezervēt savu vietu!
              </article>
            </div>

            <div class="flex">
              <div class="flex justify-start items-end w-1/2">
                <a href="https://www.bilesuparadize.lv/lv/event/154882" target="_blank" rel="noopener noreferrer">
                  <button
                      class="bg-[#5B8930] border-2 border-[#5B8930] text-white w-[6rem] hover:bg-white hover:text-[#5B8930] cursor-pointer"
                      style="aspect-ratio: 1.6">
                    Bezmaksas IELŪGUMS
                  </button>
                </a>
              </div>
              <div class="flex justify-end items-center w-1/2">
                <button
                    @click="mocartsOpen = !mocartsOpen"
                    class="bg-black text-white w-[6rem] hover:bg-white hover:text-black border-2 border-black cursor-pointer"
                    style="aspect-ratio: 1.6">
                  {{ mocartsOpen ? 'Aizvērt' : 'Lasīt' }}
                </button>
              </div>
            </div>
          </div>
        </div>

        <div class="w-full my-16 border-t border-black mx-4"></div>


        <div class="program-item mx-4">
          <div>
            <p class="font-bold text-2xl text-gray-600 uppercase">
              <span>26. septembris </span><span>16:00 </span> <span class="font-extralight">Piektdiena</span>
            </p>
          </div>

          <div class="flex flex-col py-4 gap-2 border-b border-gray-200">
            <h2 class="text-3xl font-serif">
              Garīgās mūzikas koncerts <span class="italic">Mūzika saulrieta krāsās</span>
            </h2>
          </div>

          <div class="pt-4">
            <strong>Monta Martinsone</strong> (soprāns),
            <strong>Jolanta Barinska</strong> (ērgeles)
          </div>

          <div>
            <div class="flex justify-center py-4">
              <a :href="bolderaja" target="_blank" rel="noopener noreferrer">
                <p class="hover:underline text-xl font-semibold">
                  <span class="italic pr-2">Bolderājas ev.lug. baznīca</span>
                </p>
                <p class="text-center py-2">
                  <span class="pr-2">Lielā iela 45, Rīga</span>
                  <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="currentColor"
                       class="bi bi-geo-alt-fill inline -translate-y-1" viewBox="0 0 16 16">
                    <path
                        d="M8 16s6-5.686 6-10A6 6 0 0 0 2 6c0 4.314 6 10 6 10m0-7a3 3 0 1 1 0-6 3 3 0 0 1 0 6" />
                  </svg>
                </p>
              </a>
            </div>

            <div class="description py-8 overflow-clip"
                 :class="saulrietsOpen ? '' : 'hidden'">
              <div class="w-full flex justify-center items-center pb-8">
                <div class="w-full">
                  <img src="assets/images/regence-sonore.jpg" alt=""
                       class="w-full h-full object-cover" />
                </div>
              </div>
              <article>
                Vēlā septembra vakarā aicinām uz garīgās mūzikas koncertu, kurā skanēs mūzika dvēselei — pārdomu, gaismas un mierinājuma pilna. Koncertprogrammā – sakrālās mūzikas, baroka un vēlīnās renesanses laikmeta skaņdarbi, kas izgaismo cilvēka dvēseles pārdzīvojumus un mierinājuma meklējumus Dieva mīlestībā un mūžīgajā apsolījumā.

                Muzicēs soprāns Monta Martinsone, kura izceļas ar spilgtu interpretācijas izjūtu, un ērģelniece Jolanta Barinska, kura ar ērģeļu skanējumu piešķirs šim vakaram īpašu garīguma noskaņu.
              </article>
            </div>

            <div class="flex">
              <div class="flex justify-start items-end w-1/2">
                <a href="https://www.bilesuparadize.lv/lv/event/154882" target="_blank" rel="noopener noreferrer">
                  <button
                      class="bg-[#5B8930] border-2 border-[#5B8930] text-white w-[6rem] hover:bg-white hover:text-[#5B8930] cursor-pointer"
                      style="aspect-ratio: 1.6">
                    Bezmaksas IELŪGUMS
                  </button>
                </a>
              </div>
              <div class="flex justify-end items-center w-1/2">
                <button
                    @click="saulrietsOpen = !saulrietsOpen"
                    class="bg-black text-white w-[6rem] hover:bg-white hover:text-black border-2 border-black cursor-pointer"
                    style="aspect-ratio: 1.6">
                  {{ saulrietsOpen ? 'Aizvērt' : 'Lasīt' }}
                </button>
              </div>
            </div>
          </div>
        </div>

        <div class="w-full my-16 border-t border-black mx-4"></div>


        <div class="program-item mx-4">
          <div>
            <p class="font-bold text-2xl text-gray-600 uppercase">
              <span>3. Oktobris </span><span>19:00 </span> <span class="font-extralight">Piektdiena</span>
            </p>
          </div>

          <div class="flex flex-col py-4 gap-2 border-b border-gray-200">
            <h2 class="text-3xl font-serif">Itālijas Valdzinājums</h2>
          </div>

          <div class="pt-4">
            <strong>Elīna Šimkus</strong> (soprāns),
            <strong>Māris Kupčs</strong> (klavesīns)
          </div>

          <div>
            <div class="flex justify-center py-4">
              <a :href="collegiumZale" target="_blank" rel="noopener noreferrer">
                <p class="hover:underline text-xl font-semibold">
                  Koncertzāle: <span class="italic pr-2">Collegium Musicm Riga</span>
                </p>
                <p class="text-center py-2">
                  <span class="pr-2">Vaļņu iela 9-3, Rīga</span>
                  <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="currentColor"
                       class="bi bi-geo-alt-fill inline -translate-y-1" viewBox="0 0 16 16">
                    <path
                        d="M8 16s6-5.686 6-10A6 6 0 0 0 2 6c0 4.314 6 10 6 10m0-7a3 3 0 1 1 0-6 3 3 0 0 1 0 6" />
                  </svg>
                </p>
              </a>
            </div>

            <div class="description py-8 overflow-clip"
                 :class="italijasValdzinajumsOpen ? '' : 'hidden'">
              <div class="w-full flex justify-center items-center pb-8">
                <div class="w-full">
                  <img src="assets/images/regence-sonore.jpg" alt=""
                       class="w-full h-full object-cover" />
                </div>
              </div>
              <article>
                Itālija aicina pie sevis katrā gadalaikā!  Venēcijas maģiskie kanāli, Amalfi piekraste un īsta Neapoles pica — bet šoreiz mēs ceļosim laikā un skaņās!

                3. oktobra vakarā dosimies muzikālā ceļojumā uz pavasarīgi skaisto Itāliju, kur mūs gaida 17. un 18. gadsimta itāļu komponistu spožākie meistardarbi.

                Muzicēs izcilā soprāna īpašniece Elīna Šimkus un harmoniju pavēlnieks Māris Kupčs (klavesīns), atklājot baroka Itālijas noslēpumus un kaislības mūzikā.

                Neatņemama koncerta daļa būs arī aizraujoši stāsti no Itālijas dzīves pirms dažiem gadsimtiem – ar temperamentu, smaržām un mūžīgo skaistumu.
                ​
              </article>
            </div>

            <div class="flex">
              <div class="flex justify-start items-end w-1/2">
                <a href="https://www.bilesuparadize.lv/lv/event/154877" target="_blank" rel="noopener noreferrer">
                  <button
                      class="bg-[#5B8930] border-2 border-[#5B8930] text-white w-[6rem] hover:bg-white hover:text-[#5B8930] cursor-pointer"
                      style="aspect-ratio: 1.6">
                    Biļetes
                  </button>
                </a>
              </div>
              <div class="flex justify-end items-center w-1/2">
                <button
                    @click="italijasValdzinajumsOpen = !italijasValdzinajumsOpen"
                    class="bg-black text-white w-[6rem] hover:bg-white hover:text-black border-2 border-black cursor-pointer"
                    style="aspect-ratio: 1.6">
                  {{ italijasValdzinajumsOpen ? 'Aizvērt' : 'Lasīt' }}
                </button>
              </div>
            </div>
          </div>
        </div>

        <div class="w-full my-16 border-t border-black mx-4"></div>

        <div class="program-item mx-4">
          <div>
            <p class="font-bold text-2xl text-gray-600 uppercase">
              <span>5. Oktobris </span><span>16:00 </span> <span class="font-extralight">Svētdiena</span>
            </p>
          </div>

          <div class="flex flex-col py-4 gap-2 border-b border-gray-200">
            <h2 class="text-3xl font-serif">
              Koncerts <span class="italic">The Revalers</span> (Igaunija)
            </h2>
          </div>

          <div>
            <div class="flex justify-center py-4">
              <a :href="collegiumZale" target="_blank" rel="noopener noreferrer">
                <p class="hover:underline text-xl font-semibold">
                  Koncertzāle: <span class="italic pr-2">Collegium Musicm Riga</span>
                </p>
                <p class="text-center py-2">
                  <span class="pr-2"> Vaļņu iela 9-3, Rīga</span>
                  <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="currentColor"
                       class="bi bi-geo-alt-fill inline -translate-y-1" viewBox="0 0 16 16">
                    <path
                        d="M8 16s6-5.686 6-10A6 6 0 0 0 2 6c0 4.314 6 10 6 10m0-7a3 3 0 1 1 0-6 3 3 0 0 1 0 6" />
                  </svg>
                </p>
              </a>
            </div>

            <div class="description py-8 overflow-clip"
                 :class="revalersOpen ? '' : 'hidden'">
              <div class="w-full flex justify-center items-center pb-8">
                <div class="w-full">
                  <img src="assets/images/regence-sonore.jpg" alt=""
                       class="w-full h-full object-cover" />
                </div>
              </div>
              <article>
                Igaunijas senās mūzikas ansamblis The Revalers piedāvā spilgtu un dzīvu ieskatu vēsturiskajā mūzikā, apvienojot autentisku izpildījumu ar radošu enerģiju. Ansambļa interpretācijās atdzīvojas gan baroka laikmeta elegances nianses gan radošie meklējumi. Pirmo reizi Latvijā uzstāšanos sniegs šis jaunās paaudzes ansamblis no Tallinas, kura nosaukums atsaucas uz Hanzas laikmeta pilsētu — Revali (mūsdienās Tallinu). Mūziķi spēlē vēsturiskos instrumentus un iedzīvina mūziku ar īpašu skatuvisku pievilcību un dramaturģisku izjūtu. Ansamblī muzicē Olga Kudajeva (baroka vijole, māksliniecieksā vadītāja), Tatjana Gašimova (baroka čells) un Svetlana Rodionova (klavesīns).
              </article>
            </div>

            <div class="flex">
              <div class="flex justify-start items-end w-1/2">
                <a href="https://www.bilesuparadize.lv/lv/event/154878" target="_blank" rel="noopener noreferrer">
                  <button
                      class="bg-[#5B8930] border-2 border-[#5B8930] text-white w-[6rem] hover:bg-white hover:text-[#5B8930] cursor-pointer"
                      style="aspect-ratio: 1.6">
                    Biļetes
                  </button>
                </a>
              </div>
              <div class="flex justify-end items-center w-1/2">
                <button
                    @click="revalersOpen = !revalersOpen"
                    class="bg-black text-white w-[6rem] hover:bg-white hover:text-black border-2 border-black cursor-pointer"
                    style="aspect-ratio: 1.6">
                  {{ revalersOpen ? 'Aizvērt' : 'Lasīt' }}
                </button>
              </div>
            </div>
          </div>
        </div>

        <div class="w-full my-16 border-t border-black mx-4"></div>


        <div class="program-item mx-4">
          <div>
            <p class="font-bold text-2xl text-gray-600 uppercase">
              <span>11. Oktobris </span><span>16:00 </span> <span class="font-extralight">Sestdiena</span>
            </p>
          </div>

          <div class="flex flex-col py-4 gap-2 border-b border-gray-200">
            <h2 class="text-3xl font-serif">Festivāla noslēguma koncerts</h2>
            <h3 class="text-xl font-bold">
              Ansamblis <span class="italic">Coloquio 6</span> (Hāga, NL) (S-Eeemerging)
            </h3>
          </div>

          <div>
            <div class="flex justify-center py-4">
              <a :href="collegiumZale" target="_blank" rel="noopener noreferrer">
                <p class="hover:underline text-xl font-semibold">
                  Koncertzāle: <span class="italic pr-2">Collegium Musicm Riga</span>
                </p>
                <p class="text-center py-2">
                  <span class="pr-2"> Vaļņu iela 9-3, Rīga</span>
                  <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="currentColor"
                       class="bi bi-geo-alt-fill inline -translate-y-1" viewBox="0 0 16 16">
                    <path
                        d="M8 16s6-5.686 6-10A6 6 0 0 0 2 6c0 4.314 6 10 6 10m0-7a3 3 0 1 1 0-6 3 3 0 0 1 0 6" />
                  </svg>
                </p>
              </a>
            </div>


            <div class="description py-8 overflow-clip"
                 :class="noslegumsOpen ? '' : 'hidden'">
              <div class="w-full flex justify-center items-center pb-8">
                <div class="w-full">
                  <img src="assets/images/regence-sonore.jpg" alt=""
                       class="w-full h-full object-cover" />
                </div>
              </div>
              <article>
                Noslēdzot festivālu ar spēcīgu un spilgtu akcentu, Rīgā viesosies Coloquio 6 – aizrautīgs un mūsdienīgi domājošs senās mūzikas ansamblis no Hāgas, kurš apvieno sešus talantīgus vēsturisko pūšaminstrumentu spēles meistarus.

                Coloquio 6 spēlē 18. un 19. gadsimta mūziku, izmantojot oriģinālos laikmeta instrumentus: divas vēsturiskās klarnetes, divus mežragus un divus fagotus. Šī "Harmoniemusik" konfigurācija ļauj atklāt vēsturiski autentisku, bet pārsteidzoši dzīvu un daudzkrāsainu skanējumu.

                Ansambļa nosaukums — Coloquio — nozīmē "saruna", un tieši šāda ir viņu pieeja mūzikai: dzīva un jēgpilna saruna starp laikmetiem, mūziķiem un klausītājiem. Programmās līdzās Mocarta, Haydna un citu klasicisma meistaru opusiem iekļautas arī īpašas aranžijas no tā laika operu un baletu mūzikas, kas atdzimst izsmalcinātā kamermūzikas formātā.

                Koncerts notiek ansambļa rezidences Latvijā ietvaros, S-Eeemerging programmā, kas apvieno Eiropas spilgtākos jaunos senās mūzikas māksliniekus.

                Vairāk par ansambli: <a href="https://coloquio6.com/">coloquio6.com</a>
              </article>
            </div>

            <div class="flex">
              <div class="flex justify-start items-end w-1/2">
                <a href="https://www.bilesuparadize.lv/lv/event/154879" target="_blank" rel="noopener noreferrer">
                  <button
                      class="bg-[#5B8930] border-2 border-[#5B8930] text-white w-[6rem] hover:bg-white hover:text-[#5B8930] cursor-pointer"
                      style="aspect-ratio: 1.6">
                    Biļetes
                  </button>
                </a>
              </div>
              <div class="flex justify-end items-center w-1/2">
                <button
                    @click="noslegumsOpen = !noslegumsOpen"
                    class="bg-black text-white w-[6rem] hover:bg-white hover:text-black border-2 border-black cursor-pointer"
                    style="aspect-ratio: 1.6">
                  {{ noslegumsOpen ? 'Aizvērt' : 'Lasīt' }}
                </button>
              </div>
            </div>
          </div>
        </div>

      </div>




    </div>
  </div>
</template>

<style scoped></style>
