<script setup>
import SuperTrivia from '../assets/SS/SuperTrivia.jpg';
import ChatIO from '../assets/SS/Chat.io.jpg';
import TODO from '../assets/SS/TODO-LIST.jpg';
import tracker from '../assets/SS/Expense-Tracker.jpg';
import weather from '../assets/SS/Weather.jpg';
import shopping from '../assets/SS/online-shopping-cart.jpg';

const projects = [
  {
    name: 'Super Trivia',
    stack: 'MERN, Axios, ',
    img: SuperTrivia,
    link: 'https://github.com/aliahmarizvi88/SUPER-TRIVIA',
  },
  {
    name: 'Chat.io',
    stack: 'MERN, Redux, AXIOS',
    img: ChatIO,
    link: 'https://github.com/aliahmarizvi88/Chat.io',
  },
  {
    name: 'TODO LIST',
    stack: 'MERN, Redux, AXIOS',
    img: TODO,
    link: 'https://github.com/aliahmarizvi88/TODO-LIST',
  },
  {
    name: 'Expense Tracker',
    stack: 'React, Context API, Axios',
    img: tracker,
    link: 'https://github.com/aliahmarizvi88/expense-tracker',
  },
  {
    name: 'Weather App',
    stack: 'React, Context API, Axios',
    img: weather,
    link: 'https://github.com/aliahmarizvi88/WEATHER_APP2.0',
  },
  {
    name: 'Online Shopping Card',
    stack: 'React, Context API, Axios',
    img: shopping,
    link: 'https://github.com/aliahmarizvi88/online-shopping-cart',
  },
];
</script>

<template>
  <div
    class="w-[1000px] text-black bg-white rounded-2xl flex flex-col px-10 py-12 gap-3"
  >
    <h1 class="text-4xl font-bold">Projects</h1>

    <div class="mt-10 grid grid-cols-2 gap-6">
      <div
        v-for="project in projects"
        :key="project.name"
        class="flex flex-col bg-gray-100 rounded-lg overflow-hidden shadow-md duration-300 hover:scale-105"
      >
        <a :href="project.link" target="_blank">
          <img :src="project.img" alt="" class="w-full h-48 object-cover" />
          <div class="p-4 flex flex-col gap-1">
            <h2 class="font-semibold text-lg">{{ project.name }}</h2>
            <p class="text-sm text-gray-400">{{ project.stack }}</p>
          </div>
        </a>
      </div>
    </div>

    <p class="mt-20 mb-1 text-center text-sm">All right reserved 2024</p>
  </div>
</template>
