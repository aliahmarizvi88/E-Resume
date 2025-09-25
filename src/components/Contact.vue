<script setup></script>

<template>
  <div
    class="w-[1000px] text-black bg-white rounded-2xl flex flex-col px-10 py-12 gap-3"
  >
    <h1 class="text-4xl font-bold">Contact</h1>

    <div class="flex flex-col justify-center p-10 m-5">
      <h2 class="text-2xl mb-8">
        I am Alway Open to Discussing Products,
        {{ '\n' }}
        <strong>Work and Patnership</strong>
      </h2>
      <input
        type="text"
        placeholder="Name *"
        class="py-2 text-lg border-b border-gray-300 outline-0 mx-4 my-6"
      />

      <input
        type="email"
        placeholder="Email *"
        class="py-2 text-lg border-b border-gray-300 outline-0 mx-4 my-6"
      />

      <textarea
        placeholder="Your Message *"
        class="py-2 text-lg border-b border-gray-300 outline-0 mx-4 my-6"
      />

      <button
        class="w-30 h-10 rounded-xl mt-10 cursor-pointer border border-blue-500 text-blue-500 duration-300 hover:bg-blue-500 hover:text-white"
      >
        Send
      </button>
    </div>
    <p class="mt-10 mb-1 text-center text-sm">All right reserved 2024</p>
  </div>
</template>
