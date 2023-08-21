<template>
    <div :class="{ 'bg-cover': background, 'bg-center': background }" :style="`background-image: url(${background});`">
      <div class="min-h-screen flex items-center justify-center text-center">
        <div class="bg-white p-8 rounded-md shadow-lg max-w-xl mx-auto">
          <h1 class="text-3xl font-semibold mb-4">Welcome to Our Landing Page!</h1>
          <p class="mb-4">Discover amazing content, features, and more!</p>
          <button class="bg-blue-500 text-white px-6 py-2 rounded hover:bg-blue-600">Learn More</button>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
    const background = ref('/amazing-bg.png')
  </script>
  
  <style scoped>
  </style>
  