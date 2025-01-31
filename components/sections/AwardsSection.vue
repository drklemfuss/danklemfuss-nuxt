<template>
  <section id="awards" class="timeline py-16">
    <h2 class="text-4xl font-semibold text-center mb-8">Awards</h2>
    <div class="award-container flex flex-col items-center space-y-8 m-8">
      <!-- Award Card -->
      <div
        v-for="(award, index) in awards"
        :key="index"
        class="award-item flex flex-col items-center justify-between max-w-7xl w-full border border-gray-500 p-8 rounded-2xl bg-gradient-to-tr from-violet-900 to-gray-900 mb-4 shadow-md shadow-black"
      >
        <h3 class="text-2xl text-center text-white font-semibold w-full mb-2">
          {{ award.title }}
        </h3>
        <img :src="award.logo" class="h-12 w-auto" />
        <span class="text-center text-sm text-gray-500 w-full mb-4">
          {{ award.date }}
        </span>
        <div class="flex flex-col md:flex-row w-full">
          <p class="text-gray-400 md:w-1/2 w-full p-4">
            {{ award.description }}
          </p>
          <div class="md:w-1/2 w-full">
            <img
              :src="award.image"
              alt="Award Image"
              class="w-full h-full max-h-[500px] object-cover rounded-md shadow-md shadow-black"
            />
          </div>
        </div>
        <div v-if="award.externalLink" class="w-full text-center mt-4">
          <a
            :href="award.externalLink"
            target="_blank"
            rel="noopener noreferrer"
            class="inline-block px-6 py-2 bg-purple-600 text-white font-semibold rounded-lg hover:bg-purple-700 transition"
          >
            {{ award.externalLinkText }}
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import award4Logo from "~/assets/images/logos/NAVSEA_logo.jpg";
import award4Image from "~/assets/images/awards/IMG_3094.jpg";
import award3Image from "~/assets/images/awards/sectional.webp";
import award3Logo from "~/assets/images/logos/LHX.png";
import award2Image from "~/assets/images/awards/EnRoute Coverage Map 12-12-24.png";
import award2Logo from "~/assets/images/logos/LHX.png";
import award1Image from "~/assets/images/awards/flag.jpg";
import award1Logo from "~/assets/images/logos/us-army-logo.png";

const awards = [
  {
    title:
      "NSWC PCD 2023 Annual Award (Certificate of Outstanding Program Success)",
    subtitle: "Naval Surface Warfare Center - Panama City Division",
    logo: award4Logo,
    description:
      "“For groundbreaking engineering design, integration, partnering, and testing achievements while serving the Adaptive Persistent Awareness Systems Program’s Counter-Unmanned Aircraft Systems Team at the Naval Surface Warfare Center Panama City Division. The team surpassed all obstacles and expectations in the evaluation of commercial Counter-Unmanned Aerial Systems technologies while simultaneously delivering a Navy-built, multi-mode system-of-systems counter-drone capability. Their ability to deliver relevant solutions to deter and defeat the nations adversaries greatly impact both the Navy and Transportation Security Administration’s missions to keep the nation safe.”",
    date: "March 2024",
    externalLinkText: "View Ceremony Program",
    externalLink:
      "https://www.navsea.navy.mil/Portals/103/Documents/NSWC_PCD/Annual%20Awards/FY23_AA_program.pdf?ver=DPBXOTbB4c1z2CUkgvLwpw%3D%3D&timestamp=1713279067620",
    image: award4Image,
  },
  {
    title: "L3Harris LAUNCH Award",
    subtitle: "L3Harris Technologies",
    logo: award3Logo,
    description:
      "“Went above and beyond on tight deadlines to perform and confirm root-cause analysis of ADS-C logs to develop a plan of action to restore nominal data collection. Working overnight and on scheduled off-days to deliver valuable data to make informed decisions. This is exemplary work and a testament to Dan’s work ethic.”",
    date: "December 2020",
    image: award3Image,
  },
  {
    title: "L3Harris ASCEND Award",
    subtitle: "L3Harris Technologies",
    logo: award2Logo,
    description:
      "“Dan, this Ascend Award is provided in recognition of your dedication to the Data Comm Mission and your significant technical and leadership contributions, which were key in the FAA’s ability to reach operational acceptance of the En Route Data Comm service and achieve Key Site IOC. Your continued Above and Beyond work ethic and innovative creativity are key to this challenging program’s success.”",
    date: "March 2020",
    image: award2Image,
  },
];
</script>

<style>
.award-item {
  gap: 1rem;
}

.award-container {
  position: relative;
}
</style>
