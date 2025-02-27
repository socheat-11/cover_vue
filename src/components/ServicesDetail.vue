<template>
  <div class="bg-[]">
    <section class="max-w-screen-xl mx-auto py-10">
      <div class="text-center mb-6">
        <h2 class="text-[25px] font-semibold text-black">A Performance-driven Marketing Agency</h2>
        <p class="text-gray-400 mt-3 text-[15px]">
          This is just a simple text made for this unique and awesome template, you can replace it with any text.
        </p>
      </div>

      <div class="flex flex-wrap mt-5">
        <!-- Left Section: 1/3 width on medium screens and above -->
        <div class="w-full md:w-1/3 p-4 ">
          <div data-aos="zoom-in-down" data-aos-duration="2000"
            class="flex flex-col gap-3 rounded-md bg-white shadow-[0px_0px_6px_2px_#edf2f7]">
            <div class="p-7">
              <!-- Step 1 -->
              <div class="cursor-pointer group p-3 mb-3 rounded-md transition-all duration-300 ease-in-out"
                :class="{'bg-teal-500 text-white': activePage === 'page1', 'hover:bg-gray-200': activePage !== 'page1'}"
                @click="activePage = 'page1'">
                <h3 class="text-[15px] transition-colors duration-300 ease-in-out"
                  :class="{'text-white': activePage === 'page1', 'text-black group-hover:text-[#15b8a6]': activePage !== 'page1'}">
                  Step 1
                </h3>
                <h4 class="mt-2 font-medium text-[17px] transition-colors duration-300 ease-in-out"
                  :class="{'text-white': activePage === 'page1', 'text-black group-hover:text-[#15b8a6]': activePage !== 'page1'}">
                  SEO Audit
                </h4>
                <h5 class="mt-2 font-light text-[15px] transition-colors duration-300 ease-in-out"
                  :class="{'text-white': activePage === 'page1', 'text-black group-hover:text-[#15b8a6]': activePage !== 'page1'}">
                  We offer flexible and comprehensive online marketing plans
                </h5>
              </div>

              <div class="cursor-pointer group p-3 mb-3 rounded-md transition-all duration-300 ease-in-out"
                :class="{'bg-teal-500 text-white': activePage === 'page2', 'hover:bg-gray-200': activePage !== 'page2'}"
                @click="activePage = 'page2'">
                <h3 class="text-[15px] font-medium transition-colors duration-300 ease-in-out"
                  :class="{'text-white': activePage === 'page2', 'text-black group-hover:text-[#15b8a6]': activePage !== 'page2'}">
                  Step 2
                </h3>
                <h4 class="mt-2 text-[17px] transition-colors duration-300 ease-in-out"
                  :class="{'text-white': activePage === 'page2', 'text-black group-hover:text-[#15b8a6]': activePage !== 'page2'}">
                  SEO Audit
                </h4>
                <h5 class="mt-2 font-light text-[15px] transition-colors duration-300 ease-in-out"
                  :class="{'text-white': activePage === 'page2', 'text-black group-hover:text-[#15b8a6]': activePage !== 'page2'}">
                  We offer flexible and comprehensive online marketing plans
                </h5>
              </div>

              <div class="cursor-pointer group p-3 mb-3 rounded-md transition-all duration-300 ease-in-out"
                :class="{'bg-teal-500 text-white': activePage === 'page3', 'hover:bg-gray-200': activePage !== 'page3'}"
                @click="activePage = 'page3'">
                <h3 class="text-[15px] font-medium transition-colors duration-300 ease-in-out"
                  :class="{'text-white': activePage === 'page2', 'text-black group-hover:text-[#15b8a6]': activePage !== 'page3'}">
                  Step 3
                </h3>
                <h4 class="mt-2 text-[17px] transition-colors duration-300 ease-in-out"
                  :class="{'text-white': activePage === 'page3', 'text-black group-hover:text-[#15b8a6]': activePage !== 'page3'}">
                  SEO Audit
                </h4>
                <h5 class="mt-2 font-light text-[15px] transition-colors duration-300 ease-in-out"
                  :class="{'text-white': activePage === 'page3', 'text-black group-hover:text-[#15b8a6]': activePage !== 'page3'}">
                  We offer flexible and comprehensive online marketing plans
                </h5>
              </div>

            </div>

          </div>

        </div>

        <!-- Right Section: 2/3 width on medium screens and above -->
        <div class="w-full md:w-2/3  p-4">
          <div v-for="(service, index) in services" :key="index" data-aos="zoom-in-down" data-aos-duration="2000"
            class="flex justify-center rounded-md items-center bg-white shadow-[0px_0px_6px_2px_#edf2f7]"
            v-show="activePage === service.page">
            <div class="text-start p-7">
              <img :src="service.image" class="rounded-md" alt="">
              <h4 class="text-[17px] mt-4 transition-colors duration-300 ease-in-out">
                {{ service.title }}
              </h4>
              <p class="text-[15px] mt-3 text-gray-400">
                {{ service.description }}
              </p>
              <button
                class="mt-5 text-[#15b8a6] text-[15px] font-light transition duration-300 ease-in-out flex items-center gap-2">
                Read More
                <FontAwesomeIcon class="text-[10px] text-[#15b8a6]" :icon="faChevronRight" />
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
    ref,
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
  // Initialize AOS animation
  onMounted(() => {
    AOS.init();
  });
  // Page state for toggling content
  const activePage = ref('page1');
  // Define services data
  const services = ref([
    {
      page: 'page1',
      image: new URL('../assets/1.jpg',
      import.meta.url).href,
      title: 'SEO Audit',
      description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Itaque, impedit vitae. Nobis, similique omnis cumque sapiente laboriosam animi quod cupiditate?'
    },
    {
      page: 'page2',
      image: new URL('../assets/2.jpg',
      import.meta.url).href,
      title: 'SEO Optimization',
      description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Itaque, impedit vitae. Nobis, similique omnis cumque sapiente laboriosam animi quod cupiditate?'
    },
    {
      page: 'page3',
      image: new URL('../assets/1.jpg',
      import.meta.url).href,
      title: 'SEO Audit',
      description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Itaque, impedit vitae. Nobis, similique omnis cumque sapiente laboriosam animi quod cupiditate?'
    },
  ]);
</script>