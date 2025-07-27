<script setup>
import Tags from "@/components/Tags.vue";
const tags = ['Lexicon', 'Card', 'io']
</script>

<template>
  <div class="bg-background w-full h-dvh flex items-center justify-center px-[8%] gap-[5%]">
    <!-- Background Effect -->
    <div
        class="pointer-events-none absolute inset-0
             bg-[radial-gradient(1200px_600px_at_20%_60%,rgba(128,128,255,0.15),transparent_60%)]
             opacity-70"
        aria-hidden="true"
    ></div>

    <div class="h-full py-[10%] flex-1 flex flex-col items-start justify-around gap-30">
      <!-- Title -->
      <Tags :items="tags"/>

      <div class="flex flex-col gap-30">
        <p class="text-light-white text-xl max-w-[500px] mt-[10%] font-poppins-normal">
          Building, Learning, Testing.
        </p>
        <!-- Download -->
        <div class="flex gap-5 items-center">
          <a class="bg-primary flex-2 hover:bg-primary-dark text-nowrap transition p-20 text-2xl rounded-[50px_10px_10px_50px] text-light-white font-poppins"
             href="https://github.com/andongni0723/Lexicardio/releases/latest">
            Get started
          </a>
          <a class="border-2 flex-1 border-outline  hover:bg-primary-dark text-nowrap transition p-20 text-xl rounded-[10px_50px_50px_10px] text-light-white font-poppins"
             href="https://github.com/andongni0723/Lexicardio/">
            Source Code
          </a>
        </div>
      </div>
    </div>

    <!-- Phone Images -->
    <div class="h-full flex-1 flex items-center">
      <img class="w-[700px] h-auto" src="/images/app-view.png" alt="">
    </div>
  </div>
</template>

<style scoped>

</style>
