<template>
  <div
    class="position-detail-page bg-gradient-to-b from-gray-100 dark:from-gray-900 to-gray-500 min-h-screen py-16"
  >
    <div
      class="container max-w-4xl mx-auto bg-gray-800 p-8 rounded-2xl shadow-md"
    >
      <!-- Role and Company -->
      <h1 class="text-4xl font-bold text-white mb-4">
        {{ position.role }}
      </h1>
      <h2 class="text-xl text-purple-400 mb-6">
        <a
          :href="position.link"
          target="_blank"
          rel="noopener noreferrer"
          class="hover:underline"
        >
          {{ position.company }}
        </a>
      </h2>

      <!-- About Section -->
      <div class="about mb-8">
        <h3 class="text-2xl font-semibold text-white mb-4">About</h3>
        <p class="text-gray-300 leading-relaxed">{{ position.about }}</p>
      </div>

      <!-- Responsibilities Section -->
      <div class="responsibilities mb-8">
        <h3 class="text-2xl font-semibold text-white mb-4">Responsibilities</h3>
        <ul class="list-disc list-inside text-gray-300 space-y-2">
          <li v-for="(item, index) in position.responsibilities" :key="index">
            {{ item }}
          </li>
        </ul>
      </div>

      <!-- Accomplishments Section -->
      <div class="accomplishments mb-8">
        <h3 class="text-2xl font-semibold text-white mb-4">Accomplishments</h3>
        <ul class="list-disc list-inside text-gray-300 space-y-2">
          <li v-for="(item, index) in position.accomplishments" :key="index">
            {{ item }}
          </li>
        </ul>
      </div>

      <!-- Skills Section -->
      <div class="skills">
        <h3 class="text-2xl font-semibold text-white mb-4">Skills</h3>
        <div class="flex flex-wrap gap-2">
          <span
            v-for="(skill, index) in position.skills"
            :key="index"
            class="px-3 py-1 bg-purple-700 text-white text-sm rounded-full"
          >
            {{ skill }}
          </span>
        </div>
      </div>
    </div>
  </div>
  <!-- External Links-->
  <div v-if="position.externalLinks.length > 0">
    <h3 class="text-xl font-semibold text-gray-300 mb-4">External Links</h3>
    <div
      v-for="(link, index) in position.externalLinks"
      :key="index"
      class="mb-4"
    >
      <a
        :href="link"
        target="_blank"
        rel="noopener noreferrer"
        class="text-purple-500 hover:underline"
      >
        {{ position.externalLinksDescription[index] }}
      </a>
    </div>
  </div>
</template>

<script setup>
definePageMeta({
  title: "US Army ROTC",
});

const position = {
  role: "Systems Engineer - FAA Data Comm",
  company: "L3Harris Technologies",
  companyLink: "https://www.l3harris.com/datacomm",
  location: "Melbourne, FL",
  program: "FAA Data Comm",
  programLink: "",
  about:
    "Led transformative air-to-ground communication systems for the FAA Data Comm program. This role involved high-stakes engineering to improve aviation safety and efficiency across the United States.",
  responsibilities: [
    "Led system upgrades and integration efforts.",
    "Performed RMA analysis and service verification for FAA ground stations.",
    "Collaborated with cross-functional teams to design and implement scalable solutions.",
  ],
  accomplishments: [
    "Reduced downtime by 25% through improved system reliability.",
    "Developed tools that saved over $1M in operational costs.",
    "Successfully deployed upgrades to over 50 sites nationwide.",
  ],
  skills: [
    "Systems Engineering",
    "FAA Data Comm",
    "Cross-Functional Team Leadership",
    "Reliability Analysis",
    "Communication Protocols",
  ],
  externalLinks: [],
  externalLinksDescription: [],
};
</script>

<style scoped>
.container {
  font-family: "Inter", sans-serif;
}
</style>
