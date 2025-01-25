<template>
  <section id="awards" class="timeline py-16">
    <h2 class="text-4xl font-semibold text-center mb-8">Awards</h2>
    <div class="timeline-container flex flex-col items-center space-y-8 m-8">
      <router-link
        v-for="(award, index) in awards"
        :key="index"
        :to="award.link"
        class="timeline-item group flex sm:flex-row md:flex-row items-stretch md:justify-between max-w-7xl w-full bg-gradient-to-b from-gray-700 to-gray-800 rounded-2xl overflow-hidden shadow-md shadow-black transition-all hover:scale-105 relative"
      >
        <!-- Description Section -->
        <div
          class="timeline-content flex flex-col justify-center p-6 md:w-1/2 text-left transition-all"
        >
          <h3 class="text-xl text-white font-semibold mb-2">
            {{ award.title }}
          </h3>
          <span class="text-gray-200">
            <a
              :href="award.subtitleLink"
              target="_blank"
              rel="noopener noreferrer"
              class="text-purple-500 hover:underline"
            >
              {{ award.subtitle }}
            </a>
          </span>
          <span class="text-sm text-gray-500 mb-4">{{ award.date }}</span>
          <p class="text-gray-400">{{ award.description }}</p>
        </div>

        <!-- Image Section -->
        <div class="timeline-image-container md:w-1/2 relative overflow-hidden">
          <img
            :src="award.image"
            alt="award Image"
            class="w-full h-full object-cover group-hover:opacity-100 opacity-75 transition-opacity"
          />
        </div>
      </router-link>
    </div>
  </section>
</template>

<script setup>
const awards = [
  {
    title: "",
    subtitle: "U.S. Army Reserve Officer Training Corps",
    description:
      "Built leadership skills and honed discipline as a contracted cadet while pursuing a rigorous aerospace engineering degree.",
    date: "2011 - 2015",
    link: "/position1",
    image: position1Image,
  },
];
</script>

<style>
.timeline-item {
  display: flex;
  align-items: center;
  text-align: center;
  gap: 1rem;
}

.timeline-container {
  position: relative;
}
</style>
