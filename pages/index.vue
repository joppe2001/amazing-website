<template>
  <div class="home min-h-screen">
    <section class="mt-6 py-20">
      <div class="container mx-auto px-6">
        <h1 class="text-3xl md:text-5xl font-bold mb-4">Welcome to BrandName</h1>
        <p class="text-xl md:text-2xl mb-8">Delivering the best solutions for your needs.</p>
        <a href="#services" class="text-white bg-blue-600 px-6 py-2 rounded-full hover:bg-blue-700">Discover our
          services</a>
      </div>
    </section>

    <!-- Services/Features Section -->
    <section class="home__services py-10">
      <div class="home__services__container container mx-auto px-6">
        <h2 class="text-3xl md:text-4xl font-bold mb-8">Our Services</h2>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-12">
          <nuxt-link to="/service/service-page" class="home__services-item">
            <h3 class="text-xl font-semibold mb-4">Service 1</h3>
            <p>Descriptive text about the service. Elaborate on its benefits and features.</p>
          </nuxt-link>
          <nuxt-link to="/service/service-page" class="home__services-item">
            <h3 class="text-xl font-semibold mb-4">Service 2</h3>
            <p>Descriptive text about the service. Elaborate on its benefits and features.</p>
          </nuxt-link>
          <nuxt-link to="/service/service-page" class="home__services-item">
            <h3 class="text-xl font-semibold mb-4">Service 3</h3>
            <p>Descriptive text about the service. Elaborate on its benefits and features.</p>
          </nuxt-link>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped lang="scss">
@import '../mixins/for-device.scss';

.home {
  background-image: url('../artsy-bg.png');
  background-size: cover;
  background-position: center center;
  background-repeat: no-repeat;


  &__services {
    position: relative;
    width: 100%;

    &__container {
      position: relative;
      width: 80%;
      padding: 2.5rem;
      border-radius: 1rem;
      backdrop-filter: blur(10px);
      border: 1px solid rgba(255, 255, 255, 0.125);

      @include for-device(mobile) {
        margin-bottom: 1rem;
        border: 2px solid rgba(255, 255, 255, 0.15);
        padding: 1.5rem;
      }
    }

    &-item {
      border: 1px solid rgba(255, 255, 255, 0.125);
      padding: 1rem;
      border-radius: 0.5rem;
      background-color: white;


      @include for-device(mobile) {
        margin-bottom: 1rem;
        border: 2px solid rgba(255, 255, 255, 0.25);
      }
    }
  }
}
</style>
