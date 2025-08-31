<template>
  <div class="min-h-screen bg-gradient-to-br from-gray-900 via-blue-900 to-purple-900 relative overflow-hidden">

    <div class="absolute inset-0">
      <div v-for="star in stars" :key="star.id" class="absolute w-1 h-1 bg-white rounded-full animate-pulse" :style="{
        left: star.x + '%',
        top: star.y + '%',
        animationDelay: star.delay + 's',
        opacity: star.opacity
      }">
      </div>
    </div>


    <!--<div v-for="shootingStar in shootingStars" :key="shootingStar.id"
     class="absolute animate-shoot pointer-events-none"
     :style="{ 
       left: shootingStar.startX + '%', 
       top: shootingStar.startY + '%',
       animationDelay: shootingStar.delay + 's',
       animationDuration: shootingStar.duration + 's',
       transform: `rotate(${shootingStar.angle}deg)`
     }">
  
  <div class="w-1 h-1 bg-white rounded-full relative">
    <div class="absolute right-1 top-0 w-12 h-0.5 bg-gradient-to-l from-white via-blue-200 to-transparent rounded-full opacity-80"></div>
    <div class="absolute right-1 top-0 w-8 h-0.5 bg-gradient-to-l from-white to-transparent rounded-full"></div>
    <div class="absolute -inset-1 bg-white rounded-full opacity-50 blur-sm"></div>
  </div>
</div>-->



    <div class="relative z-10 flex min-h-screen items-center justify-center px-8">

      <div class="max-w-7xl w-full flex items-center justify-between">

        <div class="flex-1 max-w-lg">
          <div class="text-center">

            <div class="relative inline-block mb-6">
              <img src="/me.jpg" alt="Liam Sidney Profile Picture"
                class="w-48 h-48 rounded-full border-4 border-white/20 shadow-2xl mx-auto hover:scale-105 transition-transform duration-300">
              <div class="absolute inset-0 rounded-full bg-gradient-to-tr from-blue-400/20 to-purple-400/20"></div>
            </div>


            <div class="mb-6">
              <TypedLine text="Liam Sidney" class="text-4xl lg:text-5xl font-bold text-white mb-2" />
              <div class="w-24 h-1 bg-gradient-to-r from-blue-400 to-purple-400 mx-auto rounded-full"></div>
            </div>


            <p class="text-gray-300 text-lg leading-relaxed mb-8 px-4">
              Full-stack developer creating web solutions to real world problems. Experienced in Javascript frameworks,
              cloud platforms and small scale reliable hosting.
            </p>


            <div class="flex flex-col sm:flex-row items-center justify-center gap-4 mb-8">

              <button @click="downloadResume"
                class="cursor-pointer bg-gradient-to-r from-blue-500 to-purple-600 hover:from-blue-600 hover:to-purple-700 text-white px-8 py-3 rounded-full font-semibold shadow-lg hover:shadow-xl transition-all duration-300 transform hover:scale-105 flex items-center gap-2">
                <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                    d="M12 10v6m0 0l-3-3m3 3l3-3m2 8H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z">
                  </path>
                </svg>
                Resume
              </button>



              <div class="flex gap-3">

                <a href="https://www.linkedin.com/in/liamsid/"
                  class="w-12 h-12 bg-white/10 hover:bg-blue-600 rounded-full flex items-center justify-center transition-all duration-300 hover:scale-110 backdrop-blur-sm border border-white/20">
                  <svg class="w-6 h-6 text-white" fill="currentColor" viewBox="0 0 24 24">
                    <path
                      d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z" />
                  </svg>
                </a>


                <a href="https://github.com/lilshottee101"
                  class="w-12 h-12 bg-white/10 hover:bg-gray-800 rounded-full flex items-center justify-center transition-all duration-300 hover:scale-110 backdrop-blur-sm border border-white/20">
                  <svg class="w-6 h-6 text-white" fill="currentColor" viewBox="0 0 24 24">
                    <path
                      d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z" />
                  </svg>
                </a>
              </div>
            </div>
          </div>
        </div>


        <div class="hidden lg:block w-px h-96 bg-gradient-to-b from-transparent via-white/30 to-transparent mx-8"></div>


        <div class="flex-1 max-w-2xl">
          <div class="text-center mb-8">
            <h2 class="text-3xl font-bold text-white mb-2">Technologies</h2>
            <div class="w-16 h-1 bg-gradient-to-r from-blue-400 to-purple-400 mx-auto rounded-full"></div>
          </div>


          <div class="grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-4 gap-4">
            <div v-for="tech in techs" :key="tech.name"
              class="bg-white/5 backdrop-blur-sm border border-white/10 rounded-xl p-4 hover:bg-white/10 transition-all duration-300 hover:scale-105 hover:border-white/20 group">
              <div class="flex flex-col items-center space-y-2">
                <div class="w-10 h-10 flex items-center justify-center">
                  <i :class="tech.icon" :style="{ color: tech.color }"
                    class="text-2xl group-hover:scale-110 transition-transform duration-300"></i>
                </div>
                <span class="text-white text-xs font-medium text-center">{{ tech.name }}</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue'
import TypedLine from './components/TypedLine.vue'

const stars = ref([])
const shootingStars = ref([])

const techs = ref([
  { name: "HTML5", icon: "fab fa-html5", color: "#E34F26" },
  { name: "JavaScript", icon: "fab fa-js-square", color: "#F7DF1E" },
  { name: "Python", icon: "fab fa-python", color: "#3776AB" },
  { name: "Bash", icon: "fas fa-terminal", color: "#4EAA25" },
  { name: "Azure", icon: "fab fa-microsoft", color: "#0078D4" },
  { name: "Cloudflare", icon: "fab fa-cloudflare", color: "#F38020" },
  { name: "npm", icon: "fab fa-npm", color: "#CB3837" },
  { name: "Node.js", icon: "fab fa-node-js", color: "#339933" },
  { name: "Vue.js", icon: "fab fa-vuejs", color: "#4FC08D" },
  { name: "TailwindCSS", icon: "fas fa-palette", color: "#06B6D4" },
  { name: "WordPress", icon: "fab fa-wordpress", color: "#21759B" },
  { name: "PostgreSQL", icon: "fas fa-database", color: "#336791" },
  { name: "SQLite", icon: "fas fa-database", color: "#003B57" },
  { name: "Git", icon: "fab fa-git-alt", color: "#F05032" },
  { name: "GitHub", icon: "fab fa-github", color: "#181717" },
  { name: "Docker", icon: "fab fa-docker", color: "#2496ED" },
  { name: "Adobe PS", icon: "fas fa-paint-brush", color: "#31A8FF" },
  { name: "Grafana", icon: "fas fa-chart-line", color: "#F46800" },
  { name: "Postman", icon: "fas fa-code", color: "#FF6C37" },
  { name: "Trello", icon: "fab fa-trello", color: "#0079BF" }
])

const downloadResume = () => {
  window.open('/Liam Sidney Resume.pdf', '_blank')
}

const generateStars = () => {
  for (let i = 0; i < 150; i++) {
    stars.value.push({
      id: i,
      x: Math.random() * 100,
      y: Math.random() * 100,
      opacity: Math.random() * 0.8 + 0.2,
      delay: Math.random() * 3
    })
  }
}

const generateShootingStars = () => {
  const directions = [
    { startX: -5, startY: 10, endX: 40, endY: 60 },
    { startX: 105, startY: 15, endX: 60, endY: 70 },
    { startX: -10, startY: 30, endX: 50, endY: 80 },
    { startX: 110, startY: 25, endX: 40, endY: 85 },
    { startX: -5, startY: 5, endX: 70, endY: 45 },
    { startX: 105, startY: 8, endX: 30, endY: 55 },
  ]

  for (let i = 0; i < 6; i++) {
    const direction = directions[i]
    const dx = direction.endX - direction.startX
    const dy = direction.endY - direction.startY
    const angle = Math.atan2(dy, dx) * (180 / Math.PI)

    shootingStars.value.push({
      id: i,
      startX: direction.startX,
      startY: direction.startY,
      endX: direction.endX,
      endY: direction.endY,
      delay: Math.random() * 15 + 3,
      duration: Math.random() * 1 + 0.8,
      angle
    })
  }

}

onMounted(() => {
  generateStars()
  generateShootingStars()
})
</script>

<style>
@import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css');

@keyframes twinkle {

  0%,
  100% {
    opacity: 0.3;
    transform: scale(1);
  }

  50% {
    opacity: 1;
    transform: scale(1.2);
  }
}

.animate-twinkle {
  animation: twinkle 2s ease-in-out infinite;
}

@keyframes shoot {
  0% {
    transform: translate(0, 0) rotate(-45deg);
    opacity: 0;
    filter: blur(1px);
  }

  5% {
    opacity: 1;
    filter: blur(0px);
  }

  95% {
    opacity: 0.8;
    filter: blur(0px);
  }

  100% {
    transform: translate(400px, 300px) rotate(-45deg);
    opacity: 0;
    filter: blur(2px);
  }
}

.animate-shoot {
  animation: shoot linear infinite;
}
</style>