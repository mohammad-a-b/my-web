<script setup>
import { ref } from "vue";
import Header from "./components/HeaderSection.vue";
import MenuBerger from "./components/MenuBerger.vue";
import Hero from "./components/HeroSection.vue";
import OfferSection from "./components/OfferSection.vue";
import PurchaseSection from "./components/PurchaseSection.vue";
import whatWillSection from "./components/WhatWillGetSection.vue";
import HowWorkSection from "./components/howWorkSection.vue";

const activeLink = ref("Home");
const navLinks = [
  { name: "Home", label: "Home" },
  { name: "Lessons", label: "Lessons" },
  { name: "Find Tutors", label: "Find Tutors" },
  { name: "About Us", label: "About Us" },
  { name: "Login", label: "Login" },
  { name: "Signup", label: "Sign Up" },
];

</script>
<template>
  <main>
    <Header
      :activeLink="activeLink"
      :links="navLinks"
     @update:activeLink="activeLink = $event"
      
    />

    <Hero />
    <OfferSection />
    <PurchaseSection />
    <whatWillSection />
    <HowWorkSection />
  </main>
</template>

<style>
main{
  color: #333333;
  padding: 34px 25px;
}
.line {
  width: 100px;
  height: 2px;
  background: #fb9c46;
}
</style>
