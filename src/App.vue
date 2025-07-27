<script setup>
import Tags from "@/components/Tags.vue";
import Nav from "@/Nav.vue";
import Hero from "@/Hero.vue";

</script>

<template>
  <Nav/>
  <Hero/>
  <div class="bg-background h-[300px]">
    <h1 class="text-primary-dark p-[100px] text-7xl font-poppins">Lexicon</h1>
    <!--<div class="bg-secondary h-200 rounded-[50px]"></div>-->
  </div>
</template>

<style scoped>
@keyframes float {
  0%   { transform: translateY(0) }
  50%  { transform: translateY(-4px) }
  100% { transform: translateY(0) }
}
.animate-float { animation: float 6s ease-in-out infinite; }
</style>
