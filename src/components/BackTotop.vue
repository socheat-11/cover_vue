<template>
  <button
    v-show="showButton"
    @click="scrollToTop"
    class="fixed bottom-5 hadow-[0px_0px_6px_2px_#edf2f7] right-7 bg-[#f5fbfa] text-[#002d5b] hover:text-white h-12 w-12 rounded-full shadow-lg hover:bg-[#15b8a6] transition-all duration-300"
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
