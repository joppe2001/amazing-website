<template>
    <div class="service-page-container mt-8">
        <!-- Service Content Begins Here -->
        <section class="intro container mx-auto px-6 py-20">
            <h1 class="text-4xl md:text-6xl font-bold mb-8">Service Name</h1>
            <p class="text-lg md:text-xl mb-8">
                Detailed description of the service. Elaborate on its unique value proposition, benefits, and why clients should consider it.
            </p>
            <div class="cta">
                <a href="#" class="text-white bg-blue-600 px-6 py-2 rounded-full hover:bg-blue-700">Learn More</a>
            </div>
        </section>

        <section class="features grid grid-cols-1 md:grid-cols-2 gap-12 px-6 py-20">
            <div class="feature-card p-6 rounded-lg shadow-md bg-white">
                <h3 class="text-2xl font-semibold mb-4">Feature 1</h3>
                <p>Explanation of the first feature. Describe its significance and how it stands out.</p>
            </div>
            <div class="feature-card p-6 rounded-lg shadow-md bg-white">
                <h3 class="text-2xl font-semibold mb-4">Feature 2</h3>
                <p>Insight into the second feature. Elaborate on its unique selling points and advantages.</p>
            </div>
        </section>

        <section class="testimonial container mx-auto px-6 py-20 bg-gray-100 rounded-lg">
            <h2 class="text-3xl font-bold mb-8">What our clients say</h2>
            <blockquote class="p-6 border-l-4 border-blue-600">
                <p class="mb-4">"A wonderful testimonial detailing the positive experiences of a satisfied client. Highlights the benefits and outcomes of using the service."</p>
                <footer>
                    <p class="font-bold">- Client Name, Position</p>
                </footer>
            </blockquote>
        </section>
    </div>
</template>

<script setup>
import { ref } from 'vue';

// Define your reactive variables and methods here using Composition API
const serviceName = ref('Service Name');
</script>

<style scoped lang="scss">
@import "../../mixins/for-device.scss";  // Adjust the path

.service-page-container {
    background-image: url('../../artsy-bg.png');
    background-size: cover;
    background-position: center center;
    background-repeat: no-repeat;

    .intro {
        @include for-device(mobile) {
            text-align: center;

            .cta {
                margin-top: 2rem;
            }
        }
    }

    .features {
        @include for-device(mobile) {
            grid-template-columns: 1fr;

            .feature-card {
                margin-bottom: 2rem;
            }
        }
    }

    .testimonial {
        @include for-device(mobile) {
            text-align: center;
        }
    }
}
</style>
