<template>
  <section id="experience" class="timeline py-16">
    <h2 class="text-4xl font-semibold text-center mb-8">
      Professional Experience
    </h2>
    <div class="timeline-container flex flex-col items-center space-y-8 m-8">
      <router-link
        v-for="(milestone, index) in milestones"
        :key="index"
        :to="milestone.link"
        class="timeline-item group flex flex-col md:flex-row items-stretch md:justify-between max-w-7xl w-full bg-gradient-to-b from-gray-700 to-gray-800 rounded-2xl overflow-hidden shadow-md shadow-black transition-all hover:scale-105 relative"
      >
        <!-- Description Section -->
        <div
          class="timeline-content flex flex-col justify-center p-6 md:w-1/2 text-left transition-all"
        >
          <h3 class="text-xl text-white font-semibold mb-2">
            {{ milestone.title }}
          </h3>
          <span class="text-gray-200">
            <a
              :href="milestone.subtitleLink"
              target="_blank"
              rel="noopener noreferrer"
              class="text-purple-500 hover:underline"
            >
              {{ milestone.subtitle }}
            </a>
          </span>
          <span class="text-sm text-white mb-4">{{ milestone.date }}</span>
          <p class="text-gray-300">{{ milestone.description }}</p>
        </div>

        <!-- Image Section -->
        <div class="timeline-image-container md:w-1/2 relative overflow-hidden">
          <img
            :src="milestone.image"
            alt="Milestone Image"
            class="w-full h-full object-cover group-hover:opacity-100 opacity-75 transition-opacity"
          />
        </div>
      </router-link>
    </div>
  </section>
</template>

<script setup>
import position1Image from "~/assets/images/experience/DRK_Army.jpg";
import position2Image from "~/assets/images/experience/cpdlc.webp";
import position3Image from "~/assets/images/experience/F35_PCD.avif";
import position4Image from "~/assets/images/experience/LiDAR.jpg";
import position5Image from "~/assets/images/experience/C-UAS.jpg";
import position6Image from "~/assets/images/experience/NB_Guam.webp";

const milestones = [
  {
    title: "Lead Systems Engineer",
    subtitle: "Naval Surface Warfare Center - Panama City Division (NSWC PCD)",
    subtitleLink:
      "https://www.navsea.navy.mil/Home/Warfare-Centers/NSWC-Panama-City/",
    description:
      "Led complex naval systems engineering projects, ensuring mission success across global Navy installation operations.",
    date: "2023-2024",
    link: "/position6",
    image: position6Image, // Credit: photo by dvids
  },
  {
    title: "Lead C-UAS Integration & Test Engineer",
    subtitle: "Naval Surface Warfare Center - Panama City Division (NSWC PCD)",
    subtitleLink:
      "https://www.navsea.navy.mil/Home/Warfare-Centers/NSWC-Panama-City/",
    description:
      "Directed counter-UAS system testing and integration, safeguarding critical assets from emerging aerial threats.",
    date: "2022-2023",
    link: "/position5",
    image: position5Image, // Credit: photo by Teledyne FLIR
  },
  {
    title: "Research & Development Engineer",
    subtitle: "Indus Technologies",
    subtitleLink: "https://www.industechnology.com/",
    description:
      "Pioneered advancements in autonomous systems and sensor technologies, driving R&D excellence.",
    date: "2021-2022",
    link: "/position4",
    image: position4Image, // Credit: photo by Velodyne LiDAR
  },
  {
    title: "Systems Engineer - F-35 JSF Panoramic Cockpit Display",
    subtitle: "L3Harris Technologies",
    subtitleLink:
      "https://www.l3harris.com/all-capabilities/f-35-lightning-ii-avionics",
    description:
      "Contributed to the development/test of advanced avionics for the F-35, delivering state-of-the-art cockpit technology to enhance pilot readiness.",
    date: "2021-2021",
    link: "/position3",
    image: position3Image, // Credit: photo by Ben Hendren
  },
  {
    title: "Systems Engineer - FAA Data Comm",
    subtitle: "L3Harris Technologies",
    subtitleLink: "https://www.l3harris.com/datacomm",
    description:
      "Engineered transformative air-to-ground communication systems, enhancing aviation safety and operational efficiency.",
    date: "2016-2021",
    link: "/position2",
    image: position2Image, // Credit: flightsim.io/file/79705/realacars
  },
  {
    title: "U.S. Army ROTC",
    subtitle: "U.S. Army Reserve Officer Training Corps",
    subtitleLink:
      "https://www.goarmy.com/careers-and-jobs/find-your-path/army-officers/rotc",
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
