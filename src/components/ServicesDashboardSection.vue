<template>
  <div class="bg-[#f5fbfa]">
    <section class="max-w-screen-xl mx-auto p-4 py-10" id="service">
      <div class="text-center mb-6">

        <div>
          <img src="../assets/ds.png" alt="">
        </div>
      </div>
    </section>
  </div>
</template>
<script setup>
  import {
    ref,
    onMounted
  } from 'vue';
  import AOS from 'aos';
  import 'aos/dist/aos.css';
  import {
    FontAwesomeIcon
  } from '@fortawesome/vue-fontawesome';
  import {
    faCode,
    faChevronRight
  } from '@fortawesome/free-solid-svg-icons';
  // Initialize AOS animation
  onMounted(() => {
    AOS.init();
  });
</script>