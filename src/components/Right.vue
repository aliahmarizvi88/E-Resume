<script setup>
import {
  UserRound,
  BriefcaseBusiness,
  FileUser,
  Contact,
} from 'lucide-vue-next';

defineProps(['activeTab']);
defineEmits(['change']);
</script>

<template>
  <div
    class="bg-white w-[120px] h-max rounded-2xl px-4 py-6 flex flex-col gap-5 text-black"
  >
    <div
      class="flex items-center flex-col px-4 py-5 text-[14px] rounded-2xl gap-2 cursor-pointer hover:scale-110 duration-300"
      :class="
        activeTab === 'About'
          ? 'bg-blue-500 text-white font-semibold'
          : 'bg-gray-200 text-black'
      "
      @click="$emit('change', 'About')"
    >
      <UserRound :size="22" :stroke-width="1.5" /> About
    </div>
    <div
      class="flex items-center flex-col px-4 py-5 text-[14px] rounded-2xl gap-2 cursor-pointer hover:scale-110 duration-300"
      :class="
        activeTab === 'Resume'
          ? 'bg-blue-500 text-white font-semibold'
          : 'bg-gray-200 text-black'
      "
      @click="$emit('change', 'Resume')"
    >
      <FileUser :size="22" :stroke-width="1.5" /> Resume
    </div>
    <div
      class="flex items-center flex-col px-4 py-5 text-[14px] rounded-2xl gap-2 cursor-pointer hover:scale-110 duration-300"
      :class="
        activeTab === 'Project'
          ? 'bg-blue-500 text-white font-semibold'
          : 'bg-gray-200 text-black'
      "
      @click="$emit('change', 'Project')"
    >
      <BriefcaseBusiness :size="22" :stroke-width="1.5" /> Projects
    </div>
    <div
      class="flex items-center flex-col px-4 py-5 text-[14px] rounded-2xl gap-2 cursor-pointer hover:scale-110 duration-300"
      :class="
        activeTab === 'Contact'
          ? 'bg-blue-500 text-white font-semibold'
          : 'bg-gray-200 text-black'
      "
      @click="$emit('change', 'Contact')"
    >
      <Contact :size="22" :stroke-width="1.5" /> Contact
    </div>
  </div>
</template>
