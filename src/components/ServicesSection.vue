<template>
    <div class="bg-[#f8fafc]">
      <section class="max-w-screen-xl mx-auto p-4 py-10" id="service">
        <div class="text-center mb-6">
          <h2 class="text-[25px] font-semibold text-black">Our Services</h2>
          <p class="text-gray-400 mt-3 text-[15px]">
            This is just a simple text made for this unique and awesome template, you can replace it with any text.
          </p>
        </div>
  
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-4">
          <div v-for="(service, index) in services" :key="index"
            class="bg-white shadow-[0px_0px_6px_2px_#edf2f7] group p-4 py-8 rounded-lg text-start"
            data-aos="zoom-in-down" data-aos-duration="2000">
            <!-- Dynamic Icon Box -->
            <div class="bg-[#eff9f8] group-hover:bg-[#15b8a6] h-12 w-12 flex items-center justify-center rounded-full mb-5">
              <font-awesome-icon :icon="service.icon" class="text-teal-600 group-hover:text-[#eff9f8] text-lg" />
            </div>
  
            <!-- Service Title & Description -->
            <h3 class="text-[19px] mt-5 font-semibold text-black">{{ service.title }}</h3>
            <p class="text-[15px] mt-5 text-gray-400 font-normal">{{ service.description }}</p>
  
            <button class="mt-5 text-[#15b8a6] text-[15px] font-light transition duration-300 ease-in-out flex items-center gap-2">
              Read More
              <FontAwesomeIcon class="text-[10px] text-[#15b8a6]" :icon="faChevronRight" />
            </button>
          </div>
        </div>
      </section>
    </div>

    <ServicesDetail />

    <ServicesDashboardSection />

  </template>
  
  <script setup>
  import { ref, onMounted } from 'vue';
  import AOS from 'aos';
  import 'aos/dist/aos.css';
  import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
  import { faCode, faChevronRight } from '@fortawesome/free-solid-svg-icons';
import ServicesDetail from './ServicesDetail.vue';
import ServicesDashboardSection from './ServicesDashboardSection.vue';
  
  // Initialize AOS animation
  onMounted(() => {
    AOS.init();
  });
  

  
  // Services array
  const services = ref([
    {
      title: "Grow Your Business",
      description: "If the distribution of letters and words is random, the reader will not be distracted from making.",
      icon: faCode,
    },
    {
      title: "Increase Your Reach",
      description: "Expand your audience with powerful digital marketing strategies that drive engagement.",
      icon: faCode,
    },
    {
      title: "Enhance Your Design",
      description: "Professional UI/UX services to create visually stunning and user-friendly interfaces.",
      icon: faCode,
    },
    {
      title: "Secure Your Data",
      description: "Protect your business with advanced cybersecurity measures and encrypted systems.",
      icon: faCode,
    },
  
    
  ]);
  </script>
  