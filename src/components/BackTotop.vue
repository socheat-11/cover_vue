<template>
  <button
    v-show="showButton"
    @click="scrollToTop"
    class="fixed bottom-5 right-5 bg-[#002d5b] text-white p-3 rounded-full shadow-lg hover:bg-[#004080] transition-all duration-300"
  >
    ↑
  </button>
</template>

<script>
export default {
  data() {
    return {
      showButton: false,
    };
  },
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
  },
  beforeUnmount() {
    window.removeEventListener("scroll", this.handleScroll);
  },
  methods: {
    handleScroll() {
      this.showButton = window.scrollY > 200;
    },
    scrollToTop() {
      window.scrollTo({ top: 0, behavior: "smooth" });
    },
  },
};
</script>
