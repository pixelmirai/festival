<script setup lang="ts">

</script>

<template>
  <div class="w-screen bg-black">
    <div class="w-screen ">
      <div class="flex  w-[96rem] mx-auto py-[8rem] ">
        <div class="h-[40rem] aspect-square  ">
          <div class="flex justify-start w-full h-1/2">
            <ContactMK/>
          </div>
          <div class="flex justify-end  w-full h-1/2">
            <ContactAD/>
          </div>


        </div>
        <div class="flex flex-col  justify-center items-center w-[16rem] h-[20rem] ">
          <ContactSocialIcons/>
          <div class="text-white uppercase text-xl font-extrabold py-4 ">
            <span>seko mums</span>
          </div>
        </div>
        <div class="flex flex-col justify-center items-center h-[40rem] aspect-square    ">
          <div class="flex flex-col justify-center items-center w-2/3 aspect-square ">
            <div class="w-[24rem]  ">
              <img src="assets/images/logo.webp" alt="" class="w-full h-full">
            </div>
            <div class="flex justify-center items-center text-3xl text-white    ">
              <span class="font-extralight -translate-y-[3px] ">SIA </span> <span class="italic font-serif  ml-1 "> Rīgas Senās mūzikas centrs</span>
            </div>

            <div class="flex flex-col justify-center items-center text-white h-1/3  ">
              <div class="  text-5xl  ">
                <i class="bi bi-map"></i>
              </div>
              <div class="text-2xl  ">
                <span>Vaļņu iela 9-3, Rīga, LV-1050</span>
              </div>
            </div>
          </div>



        </div>
      </div>
    </div>



        <div class="w-screen h-screen">
          <iframe class="w-full h-full" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2598.0651446728034!2d24.107608077161537!3d56.95025799912953!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x46eecfd124d75647%3A0x184f72b13af16db9!2zVmHEvMWGdSBpZWxhIDksIENlbnRyYSByYWpvbnMsIFLEq2dhLCBMVi0xMDUwLCBMYXR2aWE!5e1!3m2!1sen!2sat!4v1754053100948!5m2!1sen!2sat" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
        </div>


  </div>


</template>

<style scoped>

</style>