<script setup lang="js">

</script>

<template>
<div class="relative w-screen min-w-[360px] ">
  <header class="fixed hidde  top-0 h-[4rem] w-full order border-white  bg-[rgba(9,9,9,0.3)] z-[999] ">
    <div class="w-">
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