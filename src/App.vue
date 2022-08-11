<script setup>
import Navbar from './components/Navbar.vue';
import MyProjects from './components/MyProjects.vue';
import SelfHosted from './components/SelfHosted.vue';
import Footer from './components/Footer.vue';
</script>

<template>
  <Navbar />

  <section class="container mx-auto mt-4 max-w-5xl">
    <MyProjects />
    <hr class="mx-auto w-11/12">
    <SelfHosted />
  </section>

  <Footer />
</template>
