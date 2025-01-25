<template>
  <div class="relative h-[80vh]">
    <!-- Background -->
    <div
      class="absolute inset-0 bg-gradient-to-br from-purple-900 via-transparent to-transparent"
    ></div>
    <!-- Hero Content -->
    <section
      id="hero"
      class="relative flex flex-col md:flex-row items-center justify-center md:justify-between max-w-7xl mx-auto px-6 h-full"
    >
      <div class="text-section mt-20 md:mt-0 text-center md:text-left md:w-1/2">
        <h1
          class="text-4xl md:text-6xl font-bold mb-4"
          style="
            background: linear-gradient(to bottom, #7c3aed, #5b21b6);
            -webkit-background-clip: text;
            -moz-background-clip: text;
            -ms-background-clip: text;
            background-clip: text;
            color: transparent;
          "
        >
          Fueling Innovation with Passion and Precision.
        </h1>
        <p
          class="text-center md:text-left md:text-lg max-w-xl text-gray-900 dark:text-gray-400"
        >
          A Systems Engineer, Pilot, and Traveller driven by innovation and a
          passion for solving hard problems.
        </p>
      </div>
      <div class="image-section m-12 md:w-1/2 px-6 lg:m-24">
        <img
          :src="droneImage"
          alt="Futuristic Drone"
          class="w-full rounded-3xl shadow-md shadow-purple-900"
          style="filter: drop-shadow(0 0 15px rgba(128, 90, 213, 0.6))"
        />
      </div>
    </section>
  </div>
</template>

<script setup>
import droneImage from "~/assets/images/drone_background.webp";
</script>

<style scoped>
/*Placeholder */
</style>
