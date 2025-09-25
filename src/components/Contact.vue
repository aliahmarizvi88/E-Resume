<script setup>
const formAction = import.meta.env.VITE_FORMSPREE_URL;
</script>

<template>
  <div
    class="w-[1000px] text-black bg-white rounded-2xl flex flex-col px-10 py-12 gap-3"
  >
    <h1 class="text-4xl font-bold">Contact</h1>

    <form
      class="flex flex-col justify-center p-10 m-5"
      method="POST"
      :action="formAction"
    >
      <h2 class="text-2xl mb-8">
        I am Alway Open to Discussing Products,
        <strong>Work and Patnership</strong>
      </h2>
      <input
        type="text"
        placeholder="Name *"
        name="name"
        class="py-2 text-lg border-b border-gray-300 outline-0 mx-4 my-6"
        required
      />

      <input
        type="email"
        placeholder="Email *"
        name="email"
        class="py-2 text-lg border-b border-gray-300 outline-0 mx-4 my-6"
        required
      />

      <textarea
        placeholder="Your Message *"
        name="message"
        class="py-2 text-lg border-b border-gray-300 outline-0 mx-4 my-6"
        required
      />

      <button
        class="w-30 h-10 rounded-xl mt-10 cursor-pointer border border-blue-500 text-blue-500 duration-300 hover:bg-blue-500 hover:text-white"
        type="submit"
      >
        Send
      </button>
    </form>
    <p class="mt-10 mb-1 text-center text-sm">All right reserved 2024</p>
  </div>
</template>
