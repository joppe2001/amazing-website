<template>
    <section class="about text-gray-600 body-font min-h-screen flex">
        <div class="container px-5 py-24 mx-auto">
            <div class="text-center mb-20">
                <h1 class="sm:text-3xl text-2xl font-medium title-font text-gray-900 mb-4">About Us</h1>
                <p class="text-base leading-relaxed xl:w-2/4 lg:w-3/4 mx-auto">A brief introduction to the company.</p>
                <div class="flex mt-6 justify-center">
                    <div class="w-16 h-1 rounded-full bg-indigo-500 inline-flex"></div>
                </div>
            </div>
            <div class="flex flex-wrap -m-4">
                <div class="p-4 md:w-1/3">
                    <div class="h-full bg-gray-100 p-8 rounded">
                        <h2 class="text-xl font-medium title-font mb-5 text-gray-900">Our Mission</h2>
                        <p class="leading-relaxed mb-8">Detailed information about the company's mission.</p>
                    </div>
                </div>
                <div class="p-4 md:w-1/3">
                    <div class="h-full bg-gray-100 p-8 rounded">
                        <h2 class="text-xl font-medium title-font mb-5 text-gray-900">Our Vision</h2>
                        <p class="leading-relaxed mb-8">Explanation of the company's future goals and vision.</p>
                    </div>
                </div>
                <div class="p-4 md:w-1/3">
                    <div class="h-full bg-gray-100 p-8 rounded">
                        <h2 class="text-xl font-medium title-font mb-5 text-gray-900">Our Team</h2>
                        <p class="leading-relaxed mb-8">Introduction to key team members or the team's core values.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
  
<script setup>
  // You can add reactive properties or functions if needed
</script>
  
<style scoped>
.about {
    background-image: url('../better-bng.png');
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    background-attachment: fixed;
    display: flex;
    align-items: center;
}
</style>
  