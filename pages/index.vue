<template>
  <div class="about-page bg-gray-100 dark:bg-gray-900">
    <!-- Hero Section -->
    <HeroSection />
    <!-- Stats Ribbon -->
    <StatsRibbon />

    <!-- Professional Journey with Interactive Timeline -->
    <ExperienceTimeline />
    <!-- Education -->
    <EducationSection />
  </div>
</template>

<script setup>
import StatsRibbon from "~/components/sections/StatsRibbon.vue";
import HeroSection from "~/components/sections/HeroSection.vue";
import ExperienceTimeline from "~/components/sections/ExperienceTimeline.vue";
import EducationSection from "~/components/sections/EducationSection.vue";
const awards = [
  {
    name: "NSWC PCD",
    from: "NSWC PCD",
    description: "",
    date: "2024",
  },
];
</script>

<style scoped>
.about-page {
  font-family: "Inter", sans-serif;
}
</style>

<!--
1. About

This section introduces who you are and gives visitors an overview of your professional and personal identity.

Sub-sections:

    Introduction: A brief bio with a professional headshot, your tagline, or a mission statement.
    Skills & Tools: Highlight technical and soft skills, tools, and technologies you use.
    Fun Facts or Hobbies: A personal touch with hobbies, interests, or rotating fun facts.
    Inspirations: Share quotes, books, or ideas that shape your outlook.


-->

<!--
Framework for the "About" Page
1. Introduction

    Content:
        A brief introduction highlighting your career as a systems engineer, private pilot, and data analyst.
        Mention your passion for solving complex problems and exploring the world.
    Design:
        A professional headshot or silhouette-style image of you.
        A short tagline like: "A systems engineer with a passion for innovation, exploration, and making an impact."

2. Professional Journey

    Content:
        A high-level overview of your career milestones, starting with your Aerospace Engineering background.
        Highlight key projects (L3Harris, FAA Data Comm, APAS, CNIC Public Safety Systems).
        Mention your skills in developing tools (R/Shiny, MATLAB) and leadership roles.
    Design:
        A horizontal timeline with key milestones.
        Links to detailed case studies or write-ups (optional).

3. Personal Interests and Values

    Content:
        Hobbies like reading, hiking, kayaking, and traveling.
        Values such as family, problem-solving, and experiencing cultures.
    Design:
        A grid of cards with images representing hobbies and values.
        A quote that reflects your philosophy, e.g., "Family first, solving hard problems second, and always seeking new perspectives."

4. Unique Experiences

    Content:
        Fun and unique experiences like getting your pilot's license, traveling to six continents, trying exotic foods, scuba diving, and building AR-15s.
        Mention your passion for wildlife and seeing animals in their natural habitat.
    Design:
        A photo carousel or gallery showcasing your adventures.
        Interactive map highlighting the countries you’ve visited.

5. Closing Statement

    Content:
        Summarize your story, emphasizing your passion for innovation, exploration, and connection.
        Encourage visitors to explore your site (e.g., portfolio or blog).
    Design:
        A call-to-action button linking to your contact page or portfolio.

Creative Presentation Ideas

    Hero Section:
        Dark-themed with a glowing neon-accented tagline and a scrolling animation (e.g., "Scroll down to learn more").

    Interactive Timeline:
        Hover or click on milestones to reveal more details about your projects or achievements.

    Dynamic Fun Fact Section:
        A rotating section with fun facts about you (e.g., "Traveled to 6 continents," "Private pilot and remote pilot certified," etc.).

    Travel Map:
        A world map with clickable markers for the countries you’ve visited, showing a brief highlight of each trip.

    Thematic Colors:
        Use a dark background with vibrant neon accents for hover states, links, and interactive elements.
-->
