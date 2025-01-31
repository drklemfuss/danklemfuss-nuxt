<template>
  <div
    class="flex justify-between items-center p-4 border-b border-gray-200 dark:border-gray-700 bg-gradient-to-tr from-gray-900 to-gray-700 sticky top-0 z-50"
  >
    <span class="text-4xl font-bold text-purple-700">DRK</span>
    <!-- Hamburger Icon for Small Screens -->
    <div class="sm:hidden">
      <UButton
        icon="i-lucide-menu"
        variant="ghost"
        size="sm"
        @click="toggleMenu"
      >
        <span class="sr-only">Open Menu</span>
      </UButton>
    </div>

    <!-- Navigation Links (Hidden on Small Screens) -->
    <div class="hidden sm:flex space-x-4" :class="{ hidden: !isMenuOpen }">
      <UButton icon="i-lucide-user" to="/" variant="link" class="text-white">
        About
      </UButton>

      <!-- Portfolio Dropdown -->
      <div class="relative group">
        <UButton
          icon="i-lucide-briefcase"
          variant="link"
          class="relative text-white"
        >
          Experience
        </UButton>
        <div
          class="absolute hidden group-hover:block bg-gray-800 text-white rounded-lg shadow-lg p-4 space-y-2 z-50 w-48"
        >
          <router-link
            v-for="(milestone, index) in milestones"
            :key="index"
            :to="milestone.link"
            class="block px-4 py-2 rounded-lg hover:bg-gray-700 transition"
          >
            {{ milestone.title }}
            <p class="text-sm text-gray-500">{{ milestone.company }}</p>
          </router-link>
        </div>
      </div>
      <UButton
        icon="i-lucide-globe"
        to="/travel"
        variant="link"
        class="text-white"
      >
        Travel
      </UButton>
      <UButton
        icon="i-lucide-mail"
        to="/contact"
        variant="link"
        class="text-white"
      >
        Contact
      </UButton>
    </div>

    <!-- Dropdown Menu for Small Screens -->
    <div
      v-if="isMenuOpen"
      class="absolute top-16 left-0 w-full bg-gray-900 dark:bg-gray-800 p-4 sm:hidden"
    >
      <UButton icon="i-lucide-user" to="/" variant="ghost" block class="mb-2">
        About
      </UButton>

      <UButton
        icon="i-lucide-globe"
        to="/travel"
        variant="ghost"
        block
        class="mb-2"
      >
        Travel
      </UButton>
      <UButton icon="i-lucide-mail" to="/contact" variant="ghost" block>
        Contact
      </UButton>
    </div>

    <!-- Color Mode Button -->
    <ColorModeButton />
  </div>
</template>

<script setup>
import { ref } from "vue";

const isMenuOpen = ref(false);

function toggleMenu() {
  isMenuOpen.value = !isMenuOpen.value;
}

const milestones = [
  {
    title: "U.S. Army ROTC",
    company: "U.S. Army",
    link: "/position1",
  },
  {
    title: "Systems Engineer - FAA Data Comm",
    company: "L3Harris",
    link: "/position2",
  },
  {
    title: "Systems Engineer - F-35 JSF Panoramic Cockpit Display",
    company: "L3Harris",
    link: "/position3",
  },
  {
    title: "Research & Development Engineer",
    company: "Indus Technologies",
    link: "/position4",
  },
  {
    title: "Lead C-UAS Integration & Test Engineer",
    company: "NSWC PCD",
    link: "/position5",
  },
  {
    title: "Lead Systems Engineer",
    company: "NSWC PCD",
    link: "/position6",
  },
];
</script>
