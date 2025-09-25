<script setup>
import { ref } from 'vue';

import LeftSide from './LeftSide.vue';

import About from './About.vue';
import Resume from './Resume.vue';
import Project from './Project.vue';
import Contact from './Contact.vue';

import { Moon } from 'lucide-vue-next';
import Right from './Right.vue';

const theme = ref(false);

const toggleTheme = () => {
  theme.value = !theme.value;
};

const activeTab = ref('About');
</script>

<template>
  <div
    :class="[
      'flex flex-col transition-colors duration-500 py-10',
      theme
        ? 'bg-gradient-to-tl from-gray-900 via-gray-800 to-blue-900 text-white'
        : 'bg-gradient-to-tl from-purple-100 via-pink-100 to-blue-100',
    ]"
  >
    <div class="flex w-[1550px] mx-40 pb-10 items-center justify-between mb-10">
      <p class="font-extrabold text-xl">>> E-Resume</p>
      <button
        :class="[
          'bg-white rounded-full p-2 cursor-pointer',
          theme
            ? 'bg-gradient-to-tl from-purple-100 via-pink-100 to-blue-100 text-black'
            : 'bg-gradient-to-tl from-gray-900 via-gray-800 to-blue-900 text-white',
        ]"
        @click="toggleTheme"
      >
        <Moon />
      </button>
    </div>
    <div class="flex gap-10">
      <LeftSide />

      <About v-if="activeTab === 'About'" />
      <Resume v-if="activeTab === 'Resume'" />
      <Project v-if="activeTab === 'Project'" />
      <Contact v-if="activeTab === 'Contact'" />

      <Right :active-tab="activeTab" @change="activeTab = $event" />
    </div>
  </div>
</template>
