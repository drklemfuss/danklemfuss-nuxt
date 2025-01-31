<template>
  <section id="education">
    <div
      class="education-section bg-gradient-to-tr from-gray-700 to-gray-500 dark:from-gray-900 dark:to-gray-700 py-16"
    >
      <h2 class="text-4xl text-white font-semibold text-center mb-8">
        Education
      </h2>
      <div class="education-container flex flex-col items-center m-4">
        <div
          v-for="(education, index) in educations"
          :key="index"
          class="education-item flex flex-col md:flex-row items-start justify-between max-w-7xl w-full border border-gray-500 p-8 rounded-2xl bg-gray-200 dark:bg-gray-800 mb-4 shadow-md shadow-black"
        >
          <!-- Left Side: Degree and University Info -->
          <div class="left-side md:w-1/2">
            <h3 class="text-2xl font-bold">
              {{ education.degree }}
            </h3>
            <a
              :href="education.link"
              target="_blank"
              rel="noopener noreferrer"
              class="text-xl text-primary hover:underline"
            >
              {{ education.university }}
            </a>
            <p>Graduation: {{ education.graduation }}</p>
            <div class="university-logo my-4">
              <img
                v-if="education.image"
                :src="education.image"
                :alt="education.university + ' Logo'"
                class="w-32 h-auto"
              />
            </div>
            <p>{{ education.location }}</p>
            <p class="font-bold mt-4">
              Academic Achievements: {{ education.description }}
            </p>
          </div>

          <!-- Right Side: Highlighted Coursework -->
          <div
            class="right-side md:w-1/2 mt-4 md:mt-0 flex flex-col justify-start p-4"
          >
            <h4 class="text-xl font-semibold mb-4">Highlighted Coursework:</h4>
            <ul class="list-disc list-inside">
              <li v-for="(course, idx) in education.coursework" :key="idx">
                {{ course }}
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import erauLogo from "~/assets/images/education/ERAU.svg";
import fitLogo from "~/assets/images/education/FIT.svg";
const educations = [
  {
    degree: "Master of Science - Systems Engineering",
    university: "Florida Institute of Technology",
    description: "4.0 GPA",
    location: "Melbourne, FL",
    graduation: "2021",
    coursework: [
      "Decisions and Risk Analysis",
      "Model-Based Systems Engineering",
      "Research Methods in Systems Engineering",
      "Systems Engineering Design Project",
      "Systems Modeling & Analysis",
      "Systems Requirements Analysis",
    ],
    image: fitLogo,
    link: "https://www.fit.edu/",
  },
  {
    degree: "Bachelor of Science - Aerospace Engineering",
    university: "Embry Riddle Aeronautical University",
    description: "Honors Program",
    location: "Daytona Beach, FL",
    graduation: "2015",
    coursework: [
      "Aerodynamics I & II",
      "Aerospace Structures I & II",
      "Aerospace Engineering Materials",
      "Aircraft Detail Design",
      "Airplane Stability & Control",
      "Differential Equations & Matrix Methods",
      "Experimental Aerodynamics",
      "Flight Dynamics & Control",
      "Fluid Mechanics",
      "Physics III for Engineers",
      "Space Mechanics",
      "Thermodynamics",
      "Turbine and Rocket Engines",
    ],
    image: erauLogo,
    link: "https://www.erau.edu",
  },
];
</script>

<style scoped>
.left-side {
  border-right: 1px solid rgba(0, 0, 0, 0.1);
  padding-right: 1rem;
}

.right-side ul {
  padding-left: 1rem;
}
</style>
