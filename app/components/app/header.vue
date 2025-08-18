<script setup lang="ts">
import { ref } from 'vue'

const showMenu = ref(false)
const showAbout = ref(false)
const showOther = ref(false)

const toggleNav = () => (
  showMenu.value = !showMenu.value
)
</script>

<template>
  <div class="font-[Sarabun] bg-gray-200 max-h-screen fixed top-0 w-full">
    <!-- Start Header -->
    <div class="text-gray-600 bg-[#802918]">
      <nav class="container px-6 py-[0.8rem] mx-auto md:flex md:justify-between md:items-center shadow-xl pl-5 md:px-30 z-0 cursor-pointer">
        <div class="flex items-center justify-between">
          <NuxtLink to="/" class="flex justify-center items-center text-md font-bold text-white md:text-2xl hover:text-blue-200">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="size-8">
              <path stroke-linecap="round" stroke-linejoin="round" d="M4.26 10.147a60.438 60.438 0 0 0-.491 6.347A48.62 48.62 0 0 1 12 20.904a48.62 48.62 0 0 1 8.232-4.41 60.46 60.46 0 0 0-.491-6.347m-15.482 0a50.636 50.636 0 0 0-2.658-.813A59.906 59.906 0 0 1 12 3.493a59.903 59.903 0 0 1 10.399 5.84c-.896.248-1.783.52-2.658.814m-15.482 0A50.717 50.717 0 0 1 12 13.489a50.702 50.702 0 0 1 7.74-3.342M6.75 15a.75.75 0 1 0 0-1.5.75.75 0 0 0 0 1.5Zm0 0v-3.675A55.378 55.378 0 0 1 12 8.443m-7.007 11.55A5.981 5.981 0 0 0 6.75 15.75v-1.5" />
            </svg>
            <span class="text-center ml-2">Dev</span>
         </NuxtLink>

         <!-- Start mobile menu button -->
          <div @click="toggleNav" class="flex md:hidden">
            <button type="button" class="text-white hover:text-gray-400 focus:outline-none focus:text-gray-300">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
              </svg>
            </button>
          </div>
          <!-- End mobile menu button -->
        </div>

        <!-- Start mobile Menu open: "block", Menu closed: "hidden" -->
        <ul :class="showMenu ? 'flex' : 'hidden'" class="flex flex-col mt-8 space-y-4 text-sm md:flex md:space-y-0 md:flex-row md:items-center md:space-x-4 md:mt-0">
          <li class="text-white hover:text-indigo-400">
            <NuxtLink to="/" class="flex items-center text-md text-white md:text-md hover:text-amber-200">
              <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="size-6">
                <path d="M11.47 3.841a.75.75 0 0 1 1.06 0l8.69 8.69a.75.75 0 1 0 1.06-1.061l-8.689-8.69a2.25 2.25 0 0 0-3.182 0l-8.69 8.69a.75.75 0 1 0 1.061 1.06l8.69-8.689Z" />
                <path d="m12 5.432 8.159 8.159c.03.03.06.058.091.086v6.198c0 1.035-.84 1.875-1.875 1.875H15a.75.75 0 0 1-.75-.75v-4.5a.75.75 0 0 0-.75-.75h-3a.75.75 0 0 0-.75.75V21a.75.75 0 0 1-.75.75H5.625a1.875 1.875 0 0 1-1.875-1.875v-6.198a2.29 2.29 0 0 0 .091-.086L12 5.432Z" />
              </svg>
              หน้าแรก
            </NuxtLink>
          </li>

          <!-- Start About menu -->
          <li class="text-white hover:text-indigo-400">
            <div class="relative">
              <!-- Dropdown toggle button -->
              <button  @click="showAbout = !showAbout" class="flex items-center text-indigo-100 rounded-md focus:outline-none">
                <NuxtLink to="/" class="flex items-center text-md text-white md:text-md hover:text-amber-200">
                  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="size-6">
                    <path d="M11.584 2.376a.75.75 0 0 1 .832 0l9 6a.75.75 0 1 1-.832 1.248L12 3.901 3.416 9.624a.75.75 0 0 1-.832-1.248l9-6Z" />
                    <path fill-rule="evenodd" d="M20.25 10.332v9.918H21a.75.75 0 0 1 0 1.5H3a.75.75 0 0 1 0-1.5h.75v-9.918a.75.75 0 0 1 .634-.74A49.109 49.109 0 0 1 12 9c2.59 0 5.134.202 7.616.592a.75.75 0 0 1 .634.74Zm-7.5 2.418a.75.75 0 0 0-1.5 0v6.75a.75.75 0 0 0 1.5 0v-6.75Zm3-.75a.75.75 0 0 1 .75.75v6.75a.75.75 0 0 1-1.5 0v-6.75a.75.75 0 0 1 .75-.75ZM9 12.75a.75.75 0 0 0-1.5 0v6.75a.75.75 0 0 0 1.5 0v-6.75Z" clip-rule="evenodd" />
                    <path d="M12 7.875a1.125 1.125 0 1 0 0-2.25 1.125 1.125 0 0 0 0 2.25Z" />
                    </svg>
                  เกี่ยวกับเรา
                </NuxtLink>
                <svg class="w-5 h-5 text-indigo-100" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor">
                  <path fill-rule="evenodd" d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" clip-rule="evenodd" />
                </svg>
              </button>

              <!-- Dropdown menu -->
              <button v-if="showAbout" @click="showAbout = false" class="fixed top-0 inset-0 h-full w-full z-10 cursor-default"></button>
              <div v-if="showAbout" class="py-2 mt-2 bg-white rounded-md shadow-xl absolute lg:right-0 z-10 w-44 divide-y divide-gray-200">
                <NuxtLink to="/history" class="block px-4 py-[0.4rem] text-[1.0rem] text-gray-900 hover:bg-indigo-400 hover:text-indigo-100" index="2">
                  ประวัติความเป็นมา
                </NuxtLink>
                <NuxtLink to="/vision" class="block px-4 py-[0.4rem] text-[1.0rem] text-gray-900 hover:bg-indigo-400 hover:text-indigo-100" index="3">
                  วิสัยทัศน์และพันธกิจ</NuxtLink>
                <NuxtLink to="/boss" class="block px-4 py-[0.4rem] text-[1.0rem] text-gray-900 hover:bg-indigo-400 hover:text-indigo-100" index="4">
                  คณะผู้บริหาร
                </NuxtLink>
                <NuxtLink to="/executive" class="block px-4 py-[0.4rem] text-[1.0rem] text-gray-900 hover:bg-indigo-400 hover:text-indigo-100" index="5">
                  ทำเนียบผู้บริหาร
                </NuxtLink>
                <NuxtLink to="/staff" class="block px-4 py-[0.4rem] text-[1.0rem] text-gray-900 hover:bg-indigo-400 hover:text-indigo-100" index="6"> 
                  คณะผู้บริหาร
                </NuxtLink>
                <NuxtLink to="/map" class="block px-4 py-[0.4rem] text-[1.0rem] text-gray-900 hover:bg-indigo-400 hover:text-indigo-100" index="7">
                  แผนที่วิทยาลัย
                </NuxtLink>
                <NuxtLink to="/contact" class="block px-4 py-[0.4rem] text-[1.0rem] text-gray-900 hover:bg-indigo-400 hover:text-indigo-100" index="8">
                  ติดต่อวิทยาลัย
                </NuxtLink>
              </div>

            </div>
          </li>
          <!-- End About menu -->

           <!-- Start Boss menu -->
          <li class="text-white hover:text-indigo-400">
            <NuxtLink to="/" class="flex items-center text-md text-white md:text-md hover:text-amber-200">
              <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="size-6">
                <path fill-rule="evenodd" d="M8.25 6.75a3.75 3.75 0 1 1 7.5 0 3.75 3.75 0 0 1-7.5 0ZM15.75 9.75a3 3 0 1 1 6 0 3 3 0 0 1-6 0ZM2.25 9.75a3 3 0 1 1 6 0 3 3 0 0 1-6 0ZM6.31 15.117A6.745 6.745 0 0 1 12 12a6.745 6.745 0 0 1 6.709 7.498.75.75 0 0 1-.372.568A12.696 12.696 0 0 1 12 21.75c-2.305 0-4.47-.612-6.337-1.684a.75.75 0 0 1-.372-.568 6.787 6.787 0 0 1 1.019-4.38Z" clip-rule="evenodd" />
                <path d="M5.082 14.254a8.287 8.287 0 0 0-1.308 5.135 9.687 9.687 0 0 1-1.764-.44l-.115-.04a.563.563 0 0 1-.373-.487l-.01-.121a3.75 3.75 0 0 1 3.57-4.047ZM20.226 19.389a8.287 8.287 0 0 0-1.308-5.135 3.75 3.75 0 0 1 3.57 4.047l-.01.121a.563.563 0 0 1-.373.486l-.115.04c-.567.2-1.156.349-1.764.441Z" />
              </svg>
              ฝ่ายบริหาร
            </NuxtLink>
          </li>
          <!-- End Boss menu -->

          <!-- Start Department menu -->
          <li class="text-white hover:text-indigo-400">
            <NuxtLink to="/" class="flex items-center text-md text-white md:text-md hover:text-amber-200">
              <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="size-6">
                <path fill-rule="evenodd" d="M1.5 7.125c0-1.036.84-1.875 1.875-1.875h6c1.036 0 1.875.84 1.875 1.875v3.75c0 1.036-.84 1.875-1.875 1.875h-6A1.875 1.875 0 0 1 1.5 10.875v-3.75Zm12 1.5c0-1.036.84-1.875 1.875-1.875h5.25c1.035 0 1.875.84 1.875 1.875v8.25c0 1.035-.84 1.875-1.875 1.875h-5.25a1.875 1.875 0 0 1-1.875-1.875v-8.25ZM3 16.125c0-1.036.84-1.875 1.875-1.875h5.25c1.036 0 1.875.84 1.875 1.875v2.25c0 1.035-.84 1.875-1.875 1.875h-5.25A1.875 1.875 0 0 1 3 18.375v-2.25Z" clip-rule="evenodd" />
              </svg>
              สาขาวิชา
            </NuxtLink>
          </li>
          <!-- End Department menu -->
          
          <!-- Start Curriculum menu -->
          <li class="text-white hover:text-indigo-400">
            <NuxtLink to="/" class="flex items-center text-md text-white md:text-md hover:text-amber-200">
              <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="size-6">
                <path d="M11.7 2.805a.75.75 0 0 1 .6 0A60.65 60.65 0 0 1 22.83 8.72a.75.75 0 0 1-.231 1.337 49.948 49.948 0 0 0-9.902 3.912l-.003.002c-.114.06-.227.119-.34.18a.75.75 0 0 1-.707 0A50.88 50.88 0 0 0 7.5 12.173v-.224c0-.131.067-.248.172-.311a54.615 54.615 0 0 1 4.653-2.52.75.75 0 0 0-.65-1.352 56.123 56.123 0 0 0-4.78 2.589 1.858 1.858 0 0 0-.859 1.228 49.803 49.803 0 0 0-4.634-1.527.75.75 0 0 1-.231-1.337A60.653 60.653 0 0 1 11.7 2.805Z" />
                <path d="M13.06 15.473a48.45 48.45 0 0 1 7.666-3.282c.134 1.414.22 2.843.255 4.284a.75.75 0 0 1-.46.711 47.87 47.87 0 0 0-8.105 4.342.75.75 0 0 1-.832 0 47.87 47.87 0 0 0-8.104-4.342.75.75 0 0 1-.461-.71c.035-1.442.121-2.87.255-4.286.921.304 1.83.634 2.726.99v1.27a1.5 1.5 0 0 0-.14 2.508c-.09.38-.222.753-.397 1.11.452.213.901.434 1.346.66a6.727 6.727 0 0 0 .551-1.607 1.5 1.5 0 0 0 .14-2.67v-.645a48.549 48.549 0 0 1 3.44 1.667 2.25 2.25 0 0 0 2.12 0Z" />
                <path d="M4.462 19.462c.42-.419.753-.89 1-1.395.453.214.902.435 1.347.662a6.742 6.742 0 0 1-1.286 1.794.75.75 0 0 1-1.06-1.06Z" />
              </svg>
              หลักสูตร
            </NuxtLink>
          </li>
          <!-- End Curriculum menu -->

          <!-- Start Student Regsitetr menu -->
          <li class="text-white hover:text-indigo-400">
            <NuxtLink to="/" class="flex items-center text-md text-white md:text-md hover:text-amber-200">
              <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="size-6">
                <path d="M4.5 6.375a4.125 4.125 0 1 1 8.25 0 4.125 4.125 0 0 1-8.25 0ZM14.25 8.625a3.375 3.375 0 1 1 6.75 0 3.375 3.375 0 0 1-6.75 0ZM1.5 19.125a7.125 7.125 0 0 1 14.25 0v.003l-.001.119a.75.75 0 0 1-.363.63 13.067 13.067 0 0 1-6.761 1.873c-2.472 0-4.786-.684-6.76-1.873a.75.75 0 0 1-.364-.63l-.001-.122ZM17.25 19.128l-.001.144a2.25 2.25 0 0 1-.233.96 10.088 10.088 0 0 0 5.06-1.01.75.75 0 0 0 .42-.643 4.875 4.875 0 0 0-6.957-4.611 8.586 8.586 0 0 1 1.71 5.157v.003Z" />
              </svg>
              รับสมัครนักศึกษา
            </NuxtLink>
          </li>
          <!-- End Student Regsitetr menu -->

          <!-- Start Other menu -->
           <li class="text-white hover:text-indigo-400">
             <div class="relative">
              <!-- Dropdown toggle button -->
              <button @click="showOther = !showOther" class="flex items-center text-indigo-100 rounded-md focus:outline-none">
                <div class="flex items-center text-md text-white md:text-md hover:text-indigo-200">
                  <NuxtLink to="/" class="flex items-center text-md text-white md:text-md hover:text-amber-200">
                    <div class="flex items-center text-md text-white md:text-md hover:text-indigo-200"></div>
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-5 h-5">
                      <path fill-rule="evenodd" d="M9.315 7.584C12.195 3.883 16.695 1.5 21.75 1.5a.75.75 0 0 1 .75.75c0 5.056-2.383 9.555-6.084 12.436A6.75 6.75 0 0 1 9.75 22.5a.75.75 0 0 1-.75-.75v-4.131A15.838 15.838 0 0 1 6.382 15H2.25a.75.75 0 0 1-.75-.75 6.75 6.75 0 0 1 7.815-6.666ZM15 6.75a2.25 2.25 0 1 0 0 4.5 2.25 2.25 0 0 0 0-4.5Z" clip-rule="evenodd" />
                      <path d="M5.26 17.242a.75.75 0 1 0-.897-1.203 5.243 5.243 0 0 0-2.05 5.022.75.75 0 0 0 .625.627 5.243 5.243 0 0 0 5.022-2.051.75.75 0 1 0-1.202-.897 3.744 3.744 0 0 1-3.008 1.51c0-1.23.592-2.323 1.51-3.008Z" />
                    </svg>
                    เว็บอื่นๆ
                  </NuxtLink>
                </div>
                <svg class="w-5 h-5 text-indigo-100" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor">
                  <path fill-rule="evenodd" d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" clip-rule="evenodd" />
                </svg>
              </button>

              <!-- Dropdown menu -->
              <button v-if="showOther" @click="showOther = false" class="fixed top-0 inset-0 h-full w-full z-10 cursor-default"></button>
              <div v-show="showOther" class="absolute md:right-0 w-48 py-2 mt-2 bg-white rounded-md shadow-xl z-20 divide-y divide-gray-200">
                <a href="https://www.trattc.ac.th/" target="_blank" class=" block px-4 py-2 text-[1.0rem] text-gray-900 hover:bg-indigo-400 hover:text-indigo-100">
                  วท.ตราด
                </a>
                <a href="https://www.vec.go.th/" target="_blank" class=" block px-4 py-2 text-[1.0rem] text-gray-900 hover:bg-indigo-400 hover:text-indigo-100">
                  อาชีวศึกษา
                </a>
                <a href="https://www.moe.go.th/" target="_blank" class=" block px-4 py-2 text-[1.0rem] text-gray-900 hover:bg-indigo-400 hover:text-indigo-100">
                  กระทรวงศึกษาธิการ
                </a>
              </div>

            </div>
          </li>
          <!-- End Other menu -->

        </ul>
        <!-- End mobile Menu open: "block", Menu closed: "hidden" -->

      </nav>
    </div>
    <!-- End Header -->

    <!-- Start Line Navbar -->
    <div class="py-[0.16rem] flex w-full bg-white"></div>
    <!-- End Line Navbar -->
  </div>
</template>

<style>

</style>