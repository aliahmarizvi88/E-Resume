<script setup>
import {
  Facebook,
  Instagram,
  Linkedin,
  Github,
  Smartphone,
  Mail,
  MapPin,
  Cake,
  ArrowDownToLine,
} from 'lucide-vue-next';

import file from '../assets/Files/Resume_Syed Ali Ahmad Rizvi.pdf';
</script>

<template>
  <div
    class="h-[700px] w-[400px] text-black bg-white rounded-2xl ml-30 flex flex-col items-center p-8 gap-3 shadow-lg relative"
  >
    <div class="flex justify-center -mt-20">
      <img
        src="/src/assets/Images/croped.png"
        alt="Profile"
        class="h-[200px] w-[200px] rounded-2xl object-cover shadow-md"
      />
    </div>

    <p class="text-xl font-bold mt-4">Syed Ali Ahmad Rizvi</p>
    <p class="text-[11px] bg-gray-100 px-3 py-1 rounded-full text-gray-500">
      Frontend Developer
    </p>

    <div class="flex gap-4 mt-3">
      <a
        href="https://www.facebook.com/profile.php?id=100061042810917"
        target="_blank"
      >
        <Facebook
          class="bg-gray-100 p-1 rounded cursor-pointer text-blue-500 hover:scale-110 duration-300"
          size="30"
        />
      </a>

      <a href="https://www.instagram.com/the_a_h_m_a_d/" target="_blank">
        <Instagram
          class="bg-gray-100 p-1 rounded cursor-pointer text-pink-500 hover:scale-110 duration-300"
          size="30"
        />
      </a>

      <a href="https://www.linkedin.com/in/syedaliahmadrizvi88" target="_blank">
        <Linkedin
          class="bg-gray-100 p-1 rounded cursor-pointer text-blue-800 hover:scale-110 duration-300"
          size="30"
        />
      </a>

      <a href="https://github.com/aliahmarizvi88" target="_blank">
        <Github
          class="bg-gray-100 p-1 rounded cursor-pointer text-gray-600 hover:scale-110 duration-300"
          size="30"
        />
      </a>
    </div>

    <div class="mt-6 w-full bg-gray-100 rounded-xl overflow-hidden">
      <div class="flex items-center gap-3 px-4 py-3 border-b">
        <Smartphone :size="22" :stroke-width="1.5" class="text-pink-600" />
        <div>
          <p class="text-[11px] text-gray-400">Phone</p>
          <p class="text-[12px]">+92 323 445025</p>
        </div>
      </div>

      <div class="flex items-center gap-3 px-4 py-3 border-b">
        <Mail :size="22" :stroke-width="1.5" class="text-green-600" />
        <div>
          <p class="text-[11px] text-gray-400">Email</p>
          <p class="text-[12px]">aliahmadrizvi88.com</p>
        </div>
      </div>

      <div class="flex items-center gap-3 px-4 py-3 border-b">
        <MapPin :size="22" :stroke-width="1.5" class="text-pink-500" />
        <div>
          <p class="text-[11px] text-gray-400">Location</p>
          <p class="text-[12px]">Lahore, Pakistan</p>
        </div>
      </div>

      <div class="flex items-center gap-3 px-4 py-3">
        <Cake :size="22" :stroke-width="1.5" class="text-purple-600" />
        <div>
          <p class="text-[11px] text-gray-400">Birthday</p>
          <p class="text-[12px]">10 April 2002</p>
        </div>
      </div>
    </div>

    <button
      class="mt-5 py-2 px-5 text-white rounded-xl bg-blue-500 hover:scale-110 duration-300"
    >
      <a
        :href="file"
        download
        class="flex gap-2 items-center font-semibold cursor-pointer"
      >
        <ArrowDownToLine :size="20" :stroke-width="2" />
        Download CV
      </a>
    </button>
  </div>
</template>
