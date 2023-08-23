<template>
    <div class="contact-page">
      <h2>Contact Us</h2>
      
      <!-- Email Link -->
      <a :href="'mailto:' + email + '?body=Dear joppe'">Email Us</a>
      
      <!-- Phone Link (For mobile devices) -->
      <a v-if="isMobile" :href="'tel:' + phoneNumber">Call Us</a>
    </div>
  </template>
  
  <script setup>
  const email = ref('joppe@touchwonders.com') // Replace with your email
  const phoneNumber = ref('+31 6 16163382') // Replace with your phone number
  const isMobile = ref(false)
  
  let resizeHandler
  
  onMounted(() => {
    resizeHandler = () => {
      isMobile.value = window.innerWidth <= 768
    }
  
    window.addEventListener('resize', resizeHandler)
    resizeHandler() // Initial check
  })
  
  onUnmounted(() => {
    window.removeEventListener('resize', resizeHandler)
  })
  </script>
  
  <style scoped>
  .contact-page {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100vh;
  }
  
  a {
    margin: 10px;
    color: #007BFF;
    text-decoration: none;
  }
  </style>
  