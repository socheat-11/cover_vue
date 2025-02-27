<template>
    <div v-if="loading" class="fixed inset-0 flex items-center justify-center bg-white bg-opacity-75">
      <div class="w-12 h-12 border-4 border-t-[#002d5b] border-gray-300 rounded-full animate-spin"></div>
    </div>
  </template>
  
  <script setup>
  defineProps({
    loading: Boolean, // Accepts a boolean prop
  });
  </script>
  