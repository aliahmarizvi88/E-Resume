<script setup>
import { GraduationCap, BriefcaseBusiness } from 'lucide-vue-next';

const skills = [
  { name: 'HTML, CSS, Javascrpit', percent: 85, color: 'bg-indigo-400' },
  { name: 'React JS', percent: 80, color: 'bg-pink-400' },
  { name: 'Vue 3', percent: 60, color: 'bg-purple-400' },
  { name: 'Node JS', percent: 40, color: 'bg-blue-400' },
];

const Certification = [
  {
    name: 'Introduction to Front-End Development',
    link: 'https://coursera.org/verify/4Q5UBEYJEJCF',
  },
  {
    name: 'HTML and CSS in depth',
    link: 'https://coursera.org/verify/2YYGRWQABG9V',
  },

  {
    name: 'Programming with JavaScript',
    link: 'https://coursera.org/verify/UEC8WDYJ4EDC',
  },
  {
    name: 'Frontend Developer (React) Certificate',
    link: 'https://www.hackerrank.com/certificates/2646d49fbe46',
  },
  {
    name: 'Introduction to Back-End Development',
    link: 'https://coursera.org/verify/FZX8D5RSYWZ6',
  },
  {
    name: 'Work Smarter, Not Harder',
    link: 'https://coursera.org/verify/X4GDN2WNQV3R',
  },
];
</script>

<template>
  <div
    class="w-[1000px] text-black bg-white rounded-2xl flex flex-col px-10 py-12 gap-3"
  >
    <h1 class="text-4xl font-bold">Resume</h1>
    <div class="grid grid-cols-2 mt-5 gap-5">
      <div>
        <h1 class="flex items-center gap-3 text-xl font-bold">
          <GraduationCap size="30" color="#2196F3" /> Education
        </h1>
        <div class="flex flex-col gap-5 mt-4">
          <div class="bg-purple-100 p-3 rounded-xl">
            <h3 class="text-[14px] font-extralight">2018-2020</h3>
            <p class="text-md font-bold">ICS Physics</p>
            <p class="text-[14px] font-extralight">
              Punjab College, Riwaz Garden Campus
            </p>
          </div>
          <div class="bg-orange-100 p-3 rounded-xl">
            <h3 class="text-[14px] font-extralight">2020-2024</h3>
            <p class="text-md font-bold">Bachelor's in Software Engineering</p>
            <p class="text-[14px] font-extralight">
              University of Central Punjab
            </p>
          </div>
        </div>
      </div>

      <div>
        <h1 class="flex items-center gap-3 text-xl font-bold">
          <BriefcaseBusiness size="30" color="#2196F3" />Experience
        </h1>
        <div class="flex flex-col gap-5 mt-4">
          <div class="bg-orange-100 p-3 rounded-xl">
            <h3 class="text-[14px] font-extralight">Apr-Jul 2025</h3>
            <p class="text-md font-bold">React Js Intern</p>
            <p class="text-[14px] font-extralight">Pure Logics</p>
          </div>
          <div class="bg-purple-100 p-3 rounded-xl">
            <h3 class="text-[14px] font-extralight">Current</h3>
            <p class="text-md font-bold">Frontend Intern</p>
            <p class="text-[14px] font-extralight">TechScale</p>
          </div>
        </div>
      </div>

      <div class="mt-20">
        <h1 class="flex items-center gap-3 text-xl font-bold mb-5">Skills</h1>
        <div v-for="skill in skills" :key="skill.name">
          <div class="flex justify-between mb-1 text-sm font-medium">
            <span>{{ skill.name }}</span>
            <span>{{ skill.percent }}%</span>
          </div>

          <div class="w-full bg-gray-300 h-2 rounded-full my-2">
            <div
              class="h-2 rounded-full"
              :class="skill.color"
              :style="{ width: skill.percent + '%' }"
            ></div>
          </div>
        </div>
      </div>

      <div class="mt-20">
        <h1 class="flex items-center gap-3 text-xl font-bold mb-5">
          Certification
        </h1>

        <div class="flex flex-wrap gap-3">
          <div
            v-for="Certificate in Certification"
            :key="Certificate.name"
            class="bg-gray-200 text-sm px-3 py-2 rounded shadow hover:bg-blue-500 hover:text-white duration-150 transition"
          >
            <a :href="Certificate.link" target="_blank">{{
              Certificate.name
            }}</a>
          </div>
        </div>
      </div>
    </div>

    <p class="mt-20 mb-1 text-center text-sm">All right reserved 2024</p>
  </div>
</template>
