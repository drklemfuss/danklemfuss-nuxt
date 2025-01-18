<template>
  <div
    class="flex justify-between items-center p-4 border-b border-gray-200 dark:border-gray-700 bg-gray-900 dark:bg-transparent"
  >
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
      <UButton icon="i-lucide-user" to="/" variant="link"> About </UButton>
      <UButton icon="i-lucide-briefcase" to="/portfolio" variant="link">
        Portfolio
      </UButton>
      <UButton icon="i-lucide-book-open" to="/blog" variant="link">
        Blog
      </UButton>
      <UButton icon="i-lucide-globe" to="/adventures" variant="link">
        Adventures
      </UButton>
      <UButton icon="i-lucide-mail" to="/contact" variant="link">
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
        icon="i-lucide-briefcase"
        to="/portfolio"
        variant="ghost"
        block
        class="mb-2"
      >
        Portfolio
      </UButton>
      <UButton
        icon="i-lucide-book-open"
        to="/blog"
        variant="ghost"
        block
        class="mb-2"
      >
        Blog
      </UButton>
      <UButton
        icon="i-lucide-globe"
        to="/adventures"
        variant="ghost"
        block
        class="mb-2"
      >
        Adventures
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
</script>

<style scoped>
/* Optional: Add custom styles here if needed */
</style>
