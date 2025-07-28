<script setup lang="js">

</script>

<template>
<div class="relative w-screen min-w-[360px] ">
  <header class="fixed  top-0 h-[3rem] w-full order border-white  bg-[rgba(9,9,9,0.3) z-[999] ">
    <div class="w-full h-full flex justify-end items-center">

      <a href="https://www.earlymusic.lv">
      <div class="bg-black text-white px-2 py-1 font-extrabold rounded-sm  mx-4  uppercase  ">
        <span>earlymusic.lv</span>
      </div>
      </a>

    </div>
  </header>
   
  <main class="min-h-[90vh w-screen "  >
    <slot></slot>
  </main>
  <footer>

<!--    <FooterContent/>-->
  </footer>
</div>


</template>