<template>
    <div class="service-page-container mt-8 pb-10">
        <!-- Service Content Begins Here -->
        <section class="intro container mx-auto px-6 py-20">
            <h1 class="text-4xl md:text-6xl font-bold mb-8">Service Name</h1>
            <p class="text-lg md:text-xl mb-8">
                Detailed description of the service. Elaborate on its unique value proposition, benefits, and why clients
                should consider it.
            </p>
            <div class="cta">
                <a href="#" class="text-white bg-blue-600 px-6 py-2 rounded-full hover:bg-blue-700">Learn More</a>
            </div>
        </section>
        <div class="features-container">
            <section class="features grid md:grid-cols-2 gap-12 px-6 py-20">
                <div class="feature-card p-6 rounded-lg shadow-md bg-white">
                    <h3 class="text-2xl font-semibold mb-4">Feature 1</h3>
                    <p>Explanation of the first feature. Describe its significance and how it stands out.</p>
                </div>
                <div class="feature-card p-6 rounded-lg shadow-md bg-white">
                    <h3 class="text-2xl font-semibold mb-4">Feature 2</h3>
                    <p>Insight into the second feature. Elaborate on its unique selling points and advantages.</p>
                </div>
            </section>
        </div>
        <section class="testimonial container mx-auto px-6 py-6 bg-gray-100 rounded-lg">
            <h2 class="text-3xl font-bold">What our clients say</h2>
            <blockquote class="p-6 border-l-4 border-blue-600">
                <p class="mb-4">"A wonderful testimonial detailing the positive experiences of a satisfied client.
                    Highlights the benefits and outcomes of using the service."</p>
                <footer>
                    <p class="font-bold">- Client Name, Position</p>
                </footer>
            </blockquote>
        </section>
    </div>
</template>

<script setup>
const serviceName = ref('Service Name');
</script>

<style scoped lang="scss">
@import "../../mixins/for-device.scss";

.service-page-container {
    background-image: url('../../better-bng.png');
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

    .features-container {
        display: flex;
        justify-content: center;
        width: 100%;
        
    }
    .features {
        width: 80%;
        
        backdrop-filter: blur(10px);
        margin-bottom: 8rem;
        padding: 4rem;
        border-radius: 1rem;
        border: 1px solid rgba(255, 255, 255, 0.125);

        @include for-device(mobile) {
            width: 90%;
            padding: 1rem;
            margin-bottom: 6rem;
            grid-template-columns: 1fr;
            gap: 25px;

            .feature-card {
                margin-bottom: 0;
            }
        }
    }

    .testimonial {
        @include for-device(mobile) {
            text-align: center;
            width: 90%;
        }
    }
}
</style>
