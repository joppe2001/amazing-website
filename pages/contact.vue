<template>
    <div class="container min-h-screen  mx-auto px-4 py-8">
      <div class="contact-page bg-white p-8 rounded-lg shadow-lg">
        <h2 class="text-2xl font-bold mb-4">Contact Us</h2>
        
        <a :href="'mailto:' + email + '?body=Dear joppe'" class="text-blue-600 hover:underline">Email Us</a>
        
        <a v-if="isMobile" :href="'tel:' + phoneNumber" class="text-blue-600 hover:underline">Call Us</a>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref, onMounted, onUnmounted } from 'vue';
  
  const email = ref('joppe@touchwonders.com'); // Replace with your email
  const phoneNumber = ref('+31 6 16163382'); // Replace with your phone number
  const isMobile = ref(false);
  
  let resizeHandler;
  
  onMounted(() => {
    resizeHandler = () => {
      isMobile.value = typeof window !== 'undefined' && window.innerWidth <= 768;
    };
  
    if (typeof window !== 'undefined') {
      window.addEventListener('resize', resizeHandler);
      resizeHandler(); // Initial check
    }
  });
  
  onUnmounted(() => {
    if (typeof window !== 'undefined') {
      window.removeEventListener('resize', resizeHandler);
    }
  });
  </script>
  
  <style scoped>
  .container {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background-image: url('../better-bng.png');
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
  }
  .contact-page {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
  
  a {
    margin: 10px;
    color: #007BFF;
    text-decoration: none;
  }

  
  </style>
  