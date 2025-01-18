<template>
  <div class="about-page bg-gray-900 text-white">
    <!-- Hero Section -->
    <section
      class="hero flex flex-col items-center justify-center h-screen md:h-[80vh] bg-radial-primary"
    >
      <h1 class="text-4xl md:text-6xl font-bold neon-accent mb-4">
        Fueling Innovation with Passion and Precision.
      </h1>
      <p class="text-base md:text-lg text-gray-300 max-w-xl text-center">
        A Systems Engineer, Pilot, and Explorer, driven by innovation and a
        passion for solving hard problems.
      </p>
    </section>

    <!-- Professional Journey with Interactive Timeline -->
    <section class="timeline py-16">
      <h2 class="text-4xl font-semibold text-center mb-8">
        Professional Journey
      </h2>
      <div class="timeline-container flex flex-col items-center space-y-8">
        <div
          v-for="(milestone, index) in milestones"
          :key="index"
          class="timeline-item group"
        >
          <div class="timeline-point group-hover:scale-125"></div>
          <div
            class="timeline-content max-w-md p-4 rounded-lg bg-gray-800 group-hover:bg-gray-700 transition-all"
          >
            <h3 class="text-xl font-semibold mb-2">{{ milestone.title }}</h3>
            <p class="text-gray-400">{{ milestone.description }}</p>
            <span class="text-sm text-gray-500">{{ milestone.date }}</span>
          </div>
        </div>
      </div>
    </section>

    <!-- Personal Interests and Values -->
    <section class="personal py-16 bg-gradient-to-t from-gray-900 to-gray-800">
      <h2 class="text-4xl font-semibold text-center mb-8">
        Personal Interests & Values
      </h2>
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8 px-8">
        <div
          v-for="(interest, index) in interests"
          :key="index"
          class="interest-card p-6 rounded-lg bg-gray-800 hover:bg-gray-700"
        >
          <h3 class="text-xl font-semibold mb-4">{{ interest.title }}</h3>
          <p class="text-gray-400">{{ interest.description }}</p>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
const milestones = [
  {
    title: "Started at L3Harris",
    description:
      "Began as a data analyst on the FAA Data Comm program and quickly transitioned to systems engineering.",
    date: "2016",
  },
  {
    title: "DCNS Project Lead",
    description:
      "Led system upgrades, RMA analysis, and service verification activities for FAA ground stations.",
    date: "2018",
  },
  {
    title: "DCAT2 Software Systems Engineer",
    description:
      "Developed big-data architecture and visualization tools using R/Shiny for FAA Data Comm.",
    date: "2020",
  },
  {
    title: "CNIC Public Safety Systems",
    description:
      "Led systems engineering for critical safety systems supporting Navy installations worldwide.",
    date: "2023",
  },
];

const interests = [
  {
    title: "Traveling",
    description:
      "Exploring cultures, cuisines, and wildlife across six continents.",
  },
  {
    title: "Problem-Solving",
    description:
      "Developing creative solutions to complex challenges in engineering and beyond.",
  },
  {
    title: "Family",
    description:
      "Spending quality time and creating meaningful experiences with loved ones.",
  },
];
</script>

<style scoped>
.about-page {
  font-family: "Inter", sans-serif;
}

.hero {
  text-align: center;
}

.hero {
  text-align: center;
  background: linear-gradient(
    to top right,
    var(--primary-color, #7cffcb),
    transparent 20%,
    transparent 80%,
    var(--primary-color, #7cffcb)
  );
}

.neon-accent {
  color: var(--primary-color, #7cffcb);
  text-shadow: 0 0 10px var(--primary-color, #7cffcb),
    0 0 100px var(--primary-color, #7cffcb),
    0 0 50px var(--primary-color, #7cffcb);
}

.timeline-container {
  position: relative;
}

.timeline-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  gap: 1rem;
}

.timeline-point {
  width: 1.5rem;
  height: 1.5rem;
  background-color: var(--primary-color, #7cffcb);
  border-radius: 50%;
  transition: transform 0.3s;
}

.timeline-content {
  max-width: 20rem;
  background: #2d2d2d;
  transition: background 0.3s;
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
