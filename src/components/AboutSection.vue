<template>
    <div class="">
        <section class="max-w-screen-xl mx-auto" id="about">
            <div class="flex flex-wrap py-16">
                <div class="w-full md:w-1/2 p-4 ">
                    <div data-aos="zoom-in-down" data-aos-duration="2000"
                        class="relative flex justify-center items-center w-full max-w-md mx-auto">
                        <!-- Image -->
                        <img src="../assets/about.jpg" alt="Experience" class="w-full rounded-full">

                        <!-- Centered Text Box -->
                        <div
                            class="absolute flex flex-col justify-center items-center bg-white w-40 h-40 rounded-full shadow-lg transition-all duration-300 hover:bg-teal-600 group hover:scale-105">
                            <span class="text-3xl font-bold text-teal-600 group-hover:text-white">15+</span>
                            <span class="text-sm font-semibold text-gray-700 group-hover:text-white">Years</span>
                            <span class="text-sm font-semibold text-gray-700 group-hover:text-white">Experience</span>
                        </div>
                    </div>
                </div>
                <div class="w-full md:w-1/2 p-4 flex items-center justify-center">
                    <div data-aos="zoom-in-down" data-aos-duration="2000" class="flex flex-col">
                        <h2 class="text-[15px] uppercase text-[#15b8a6] font-bold">Who Are We ?</h2>
                        <h3 class="text-black font-bold mt-3 text-[30px]">
                            We're a global stakeholder <br>
                            relations and partnership <br>
                            building consultancy.
                        </h3>
                        <h3 class="text-gray-400 mt-3 font-normal text-[15px] leading-relaxed">
                            Get instant helpful resources about anything on the go, easily implement secure money
                            transfer solutions, boost your daily efficiency, connect to other app users and create your
                            own Techwind network, and much more with just a few taps. commodo consequat. Duis aute
                            irure.
                        </h3>
                        <div>
                            <button
                                class="bg-[#15b8a6] mt-5 px-5 py-3 text-white font-semibold rounded-lg hover:bg-[#13a394] transition duration-300 ease-in-out flex items-center gap-2">
                                Read More
                                <FontAwesomeIcon class="text-[10px]" :icon="faChevronRight" />
                            </button>
                        </div>
                    </div>
                </div>
            </div>
            
        </section>
    </div>
</template>

<script setup>
    import {
        onMounted
    } from 'vue';
    import AOS from 'aos';
    import 'aos/dist/aos.css';
    import {
        FontAwesomeIcon
    } from '@fortawesome/vue-fontawesome';
    import {
        faChevronRight
    } from '@fortawesome/free-solid-svg-icons';
    onMounted(() => {
        AOS.init();
    });
</script>