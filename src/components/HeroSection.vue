<template>
    <div class="bg-[#f5fbfa]">
        <section class="max-w-screen-xl mx-auto" id="hero">
            <div class="flex flex-wrap py-10">
                <div class="w-full md:w-1/2 p-4 flex items-center justify-center">
                    <div data-aos="zoom-in-down" data-aos-duration="2000" class="flex flex-col">
                        <h2 class="text-[40px] text-black font-bold">Get Creative & <br> Modern With Upcover</h2>
                        <h3 class="text-gray-400 font-normal text-lg leading-relaxed">
                            We're a global stakeholder
                            relations and partnership
                            building consultancy.
                        </h3>
                        <h3 class="text-gray-400 font-normal text-lg leading-relaxed">
                            This is just a simple text made for this unique and
                            awesome template, you can replace it with any text.
                        </h3>
                        <div>
                            <button
                                class="bg-[#15b8a6] mt-5 px-5 py-3 text-white font-semibold rounded-lg hover:bg-[#13a394] transition duration-300 ease-in-out flex items-center gap-2">
                                Contact Us
                                <FontAwesomeIcon class="text-[10px]" :icon="faChevronRight" />
                            </button>
                        </div>
                    </div>
                </div>
                <div class="w-full md:w-1/2 p-4 ">
                    <div data-aos="zoom-in-down" data-aos-duration="2000"
                        class="flex py-24  justify-center rounded-full items-center bg-[#ddf8f4]">
                        <!-- Image -->
                        <img src="../assets/bg.png" alt="" class="w-full z-10">
                    </div>

                </div>
            </div>
        </section>
    </div>
</template>

<script setup>
import { onMounted } from 'vue';
import AOS from 'aos';
import 'aos/dist/aos.css';
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
import { faChevronRight } from '@fortawesome/free-solid-svg-icons';

onMounted(() => {
    AOS.init();
});
</script>