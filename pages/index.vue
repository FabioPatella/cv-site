<template>
  <div class="min-h-screen bg-gray-50">
    <!-- Navigation -->
    <nav class="fixed top-0 w-full bg-white/90 backdrop-blur-md border-b border-gray-200 z-50 shadow-sm">
      <div class="container mx-auto px-6 py-4">
        <div class="flex items-center justify-between">
          <h1 class="text-xl font-bold text-gray-900 hidden md:block">Fabio Patella</h1>
          <div class="flex flex-wrap gap-x-6 gap-y-2 w-full md:w-auto md:ml-8">
            <a href="#about" :class="linkClass('about')" @click.prevent="handleNavClick('about')">About</a>
            <a href="#experience" :class="linkClass('experience')" @click.prevent="handleNavClick('experience')">Experience</a>
            <a href="#education" :class="linkClass('education')" @click.prevent="handleNavClick('education')">Education</a>
            <a href="#skills" :class="linkClass('skills')" @click.prevent="handleNavClick('skills')">Skills</a>
            <a href="#projects" :class="linkClass('projects')" @click.prevent="handleNavClick('projects')">Projects</a>
            <a href="#contact" :class="linkClass('contact')" @click.prevent="handleNavClick('contact')">Contact</a>         
            <div class="flex items-center gap-1 text-sm font-medium">
  <a href="/" class="text-blue-600 underline decoration-blue-600 underline-offset-4 font-semibold">EN</a>
  <span class="text-gray-300">|</span>
  <a href="/it" class="text-gray-600 hover:text-gray-900 transition-colors">IT</a>
</div>
          </div>
        </div>
      </div>
    </nav>

    <!-- Hero Section -->
    <section id="about" class="pt-32 pb-16 px-6 bg-gray-50 scroll-mt-24">
      <div class="container mx-auto max-w-4xl">
        <div class="grid md:grid-cols-3 gap-12 items-center">
          <div class="md:col-span-2">
            <div class="inline-block bg-blue-100 text-blue-700 px-4 py-2 rounded-full text-sm font-medium mb-6">
              Software Engineer
            </div>
            <h2 class="text-5xl md:text-6xl font-bold text-gray-900 mb-6">
              Fabio Patella
            </h2>
            <p class="text-lg text-gray-700 mb-8 leading-relaxed">
              Recent graduate in Computer Science and Engineering from Politecnico di Milano, possessing cross-disciplinary skills in computer science with a specialization in software engineering. Based in Milan, Italy.
            </p>
            <div class="flex flex-wrap gap-4">
              <a href="#contact" class="bg-blue-600 text-white px-8 py-3 rounded-lg font-medium hover:bg-blue-700 transition shadow-lg">
                Get in Touch
              </a>
              <a href="https://linkedin.com/in/fabio-patella" target="_blank" class="bg-white text-gray-900 px-8 py-3 rounded-lg font-medium hover:bg-gray-50 transition shadow-md border border-gray-200">
                LinkedIn
              </a>
            </div>
          </div>
          <div class="flex justify-center md:justify-end">
            <img src="/static/images/profile.webp" alt="Fabio Patella" class="w-56 h-56 rounded-full object-cover border-4 border-blue-200 shadow-lg" />
          </div>
        </div>
      </div>
    </section>

    <!-- Experience Section -->
    <section id="experience" class="py-16 px-6 bg-gray-50 scroll-mt-24">
      <div class="container mx-auto max-w-4xl">
        <div class="text-center mb-16">
          <h3 class="text-4xl font-bold text-gray-900 mb-4">Working Experience</h3>
          <p class="text-gray-600 text-lg">Professional career and responsibilities</p>
        </div>
        
        <div class="max-w-3xl mx-auto">
          <div class="bg-gradient-to-br from-white to-gray-50 p-8 rounded-xl border border-gray-200 shadow-md hover:shadow-xl transition">
            <div class="flex justify-between items-start mb-4">
              <div>
                <h4 class="text-2xl font-bold text-gray-900 mb-2">Fullstack Developer & Application Maintenance</h4>
                <p class="text-blue-700 font-semibold text-lg">Tamtamy Reply</p>
              </div>
              <span class="text-sm text-gray-500 bg-gray-100 px-4 py-2 rounded-full font-medium whitespace-nowrap">Since Jun 2025</span>
            </div>
            
            <div class="space-y-4 mt-6">
              <div class="flex items-start gap-3">
                <div class="w-2 h-2 bg-blue-600 rounded-full mt-2 flex-shrink-0"></div>
                <div>
                  <p class="text-gray-700 font-medium mb-1">Fullstack Development (50%)</p>
                  <p class="text-gray-600 text-sm">Frontend development with Vue.js (25%) and backend development with Laravel (25%)</p>
                </div>
              </div>
              <div class="flex items-start gap-3">
                <div class="w-2 h-2 bg-blue-600 rounded-full mt-2 flex-shrink-0"></div>
                <div>
                  <p class="text-gray-700 font-medium mb-1">Application Maintenance (50%)</p>
                  <p class="text-gray-600 text-sm">Maintaining and improving existing applications, bug fixing, and performance optimization</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Education Section -->
    <section id="education" class="py-16 px-6 bg-gray-50 scroll-mt-24">
      <div class="container mx-auto max-w-4xl">
        <div class="text-center mb-16">
          <h3 class="text-4xl font-bold text-gray-900 mb-4">Education</h3>
          <p class="text-gray-600 text-lg">Academic background and qualifications</p>
        </div>
        
        <div class="relative">
          <div class="absolute left-8 top-0 bottom-0 w-0.5 bg-blue-200 hidden md:block"></div>
          
          <div class="space-y-8">
            <div v-for="edu in education" :key="edu.title" class="relative">
              <div class="md:pl-20">
                <div class="absolute left-6 w-5 h-5 bg-blue-600 rounded-full border-4 border-white hidden md:block shadow-lg"></div>
                <div class="bg-white p-8 rounded-xl shadow-md hover:shadow-xl transition border border-gray-200">
                  <div class="flex flex-col md:flex-row md:justify-between md:items-start mb-4 gap-2">
                    <div>
                      <h4 class="text-xl font-bold text-gray-900 mb-2">{{ edu.title }}</h4>
                      <p class="text-blue-700 font-semibold">{{ edu.institution }}</p>
                    </div>
                    <span class="text-sm text-gray-500 bg-gray-100 px-4 py-2 rounded-full font-medium">{{ edu.period }}</span>
                  </div>
                  <p class="text-gray-700 font-medium">{{ edu.grade }}</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="py-16 px-6 scroll-mt-24">
      <div class="container mx-auto max-w-4xl">
        <div class="text-center mb-16">
          <h3 class="text-4xl font-bold text-gray-900 mb-4">Technical Skills</h3>
          <p class="text-gray-600 text-lg">Core competencies and technical expertise</p>
        </div>
        
        <div class="grid md:grid-cols-2 gap-6">
          <div v-for="(skill, index) in skills" :key="skill.title" 
               class="bg-gradient-to-br from-white to-gray-50 p-8 rounded-xl border border-gray-200 hover:border-blue-300 hover:shadow-lg transition group">
            <div class="flex items-start gap-4">
              <div class="w-10 h-10 bg-blue-100 rounded-lg flex items-center justify-center flex-shrink-0 group-hover:bg-blue-200 transition">
                <span class="text-xl">{{ getSkillIcon(index) }}</span>
              </div>
              <div>
                <h4 class="text-lg font-semibold text-gray-900 mb-2 group-hover:text-blue-700 transition">{{ skill.title }}</h4>
                <p class="text-gray-600 text-sm leading-relaxed">{{ skill.description }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="py-16 px-6 scroll-mt-24">
      <div class="container mx-auto max-w-4xl">
        <div class="text-center mb-16">
          <h3 class="text-4xl font-bold text-gray-900 mb-4">Featured Projects</h3>
          <p class="text-gray-600 text-lg">Selected work and research experience</p>
        </div>
        
        <div class="grid md:grid-cols-2 gap-6">
          <div v-for="project in projects" :key="project.title" 
               class="bg-gradient-to-br from-white to-gray-50 p-8 rounded-xl border border-gray-200 hover:border-blue-300 hover:shadow-xl transition group">
            <div class="flex justify-between items-start mb-4">
              <h4 class="text-lg font-bold text-gray-900 group-hover:text-blue-700 transition flex-1">{{ project.title }}</h4>
              <span v-if="project.achievement" class="ml-4 text-xs bg-blue-600 text-white px-3 py-1.5 rounded-full font-semibold whitespace-nowrap flex-shrink-0">
                {{ project.achievement }}
              </span>
            </div>
            <p class="text-gray-600 leading-relaxed text-sm">{{ project.description }}</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-16 px-6 scroll-mt-24">
      <div class="container mx-auto max-w-4xl">
        <div class="text-center mb-16">
          <h3 class="text-4xl font-bold text-gray-900 mb-4">Let's Connect</h3>
          <p class="text-gray-600 text-lg">Feel free to reach out for opportunities or collaborations</p>
        </div>
        
        <div class="grid md:grid-cols-3 gap-6">
          <a href="mailto:fabio140199@gmail.com" class="bg-gradient-to-br from-blue-50 to-indigo-50 p-8 rounded-xl border border-blue-200 hover:border-blue-400 hover:shadow-xl transition group text-center">
            <div class="w-16 h-16 bg-blue-600 rounded-full flex items-center justify-center mx-auto mb-4 group-hover:scale-110 transition">
              <span class="text-3xl">📧</span>
            </div>
            <p class="text-xs text-gray-500 uppercase font-semibold tracking-wide mb-2">Email</p>
            <p class="text-gray-900 font-semibold break-all">fabio140199@gmail.com</p>
          </a>
          <a href="https://linkedin.com/in/fabio-patella" target="_blank" class="bg-gradient-to-br from-blue-50 to-indigo-50 p-8 rounded-xl border border-blue-200 hover:border-blue-400 hover:shadow-xl transition group text-center">
            <div class="w-16 h-16 bg-blue-600 rounded-full flex items-center justify-center mx-auto mb-4 group-hover:scale-110 transition">
              <span class="text-4xl">💼</span>
            </div>
            <p class="text-xs text-gray-500 uppercase font-semibold tracking-wide mb-2">LinkedIn</p>
            <p class="text-gray-900 font-semibold">fabio-patella</p>
          </a>
          <a href="https://github.com/FabioPatella" target="_blank" class="bg-gradient-to-br from-blue-50 to-indigo-50 p-8 rounded-xl border border-blue-200 hover:border-blue-400 hover:shadow-xl transition group text-center">
            <div class="w-16 h-16 bg-blue-600 rounded-full flex items-center justify-center mx-auto mb-4 group-hover:scale-110 transition">
              <span class="text-4xl">🔗</span>
            </div>
            <p class="text-xs text-gray-500 uppercase font-semibold tracking-wide mb-2">GitHub</p>
            <p class="text-gray-900 font-semibold">FabioPatella</p>
          </a>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <footer class="py-8 px-6 border-t border-gray-200 bg-gray-50">
      <div class="container mx-auto max-w-5xl text-center">
        <p class="text-gray-600">&copy; 2025 Fabio Patella. All rights reserved.</p>
      </div>
    </footer>
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted, onBeforeUnmount } from 'vue'

const currentSection = ref<string>('about')
const sectionIds = ['about', 'experience', 'education', 'skills', 'projects', 'contact']

const linkClass = (id: string) => {
  const base = 'text-gray-600 hover:text-blue-600 transition text-sm font-medium no-underline hover:underline underline-offset-8'
  const active = ' underline text-blue-600'
  return currentSection.value === id ? base + active : base
}

const handleNavClick = (id: string) => {
  const el = document.getElementById(id)
  if (!el) return
  const rect = el.getBoundingClientRect()
  const scrollTop = window.pageYOffset || document.documentElement.scrollTop || 0
  const nav = document.querySelector('nav') as HTMLElement | null
  const headerHeight = nav?.offsetHeight ?? 0
  const targetTop = rect.top + scrollTop - headerHeight - 8
  window.scrollTo({ top: Math.max(targetTop, 0), behavior: 'smooth' })
}

// Choose active section by closest-to-viewport-center (more reliable on mobile)
let ticking = false
const updateActiveSectionByCenter = () => {
  if (ticking) return
  ticking = true
  requestAnimationFrame(() => {
    const viewportCenter = window.innerHeight / 2
    let bestId = currentSection.value
    let bestDistance = Number.POSITIVE_INFINITY
    for (const id of sectionIds) {
      const el = document.getElementById(id)
      if (!el) continue
      const rect = el.getBoundingClientRect()
      const sectionCenter = rect.top + rect.height / 2
      const distance = Math.abs(sectionCenter - viewportCenter)
      if (distance < bestDistance) {
        bestDistance = distance
        bestId = id
      }
    }
    if (bestId && bestId !== currentSection.value) {
      currentSection.value = bestId
    }
    ticking = false
  })
}

onMounted(() => {
  currentSection.value = 'about'
  updateActiveSectionByCenter()
  window.addEventListener('scroll', updateActiveSectionByCenter, { passive: true })
  window.addEventListener('resize', updateActiveSectionByCenter)
  window.addEventListener('orientationchange', updateActiveSectionByCenter)
})

onBeforeUnmount(() => {
  window.removeEventListener('scroll', updateActiveSectionByCenter)
  window.removeEventListener('resize', updateActiveSectionByCenter)
  window.removeEventListener('orientationchange', updateActiveSectionByCenter)
})

const skills = [
  {
    title: 'Programming Languages',
    description: 'C, C++, C#, Java, JavaScript, Python, PHP'
  },
  {
    title: 'Database Skills',
    description: 'Conceptual and logical design, integration, and management of distributed databases, querying databases with SQL and MySQL, use of JPA library for Object/Relational Mapping'
  },
  {
    title: 'Programming Frameworks',
    description: 'Java Enterprise Edition, Java Spring and Laravel for backend programming, React and Vue for Front-End development. Technologies for distributed systems: MPI, Node-Red, Akka, Spark'
  },
  {
    title: 'Software Process Management Tools',
    description: 'Git/GitHub, Docker, testing expertise (JUnit, PyTest, Mockito), specification, verification, validation, and software design (Alloy, Uppaal), Agile software development practices (SCRUM)'
  },
  {
    title: 'Artificial Intelligence',
    description: 'Machine Learning and Data Mining (Scikit-Learn), Deep Learning (TensorFlow, Keras), Reinforcement Learning (Stable-Baselines3)'
  },
  {
    title: 'Languages',
    description: 'Italian (native speaker), English B2 level (First and TOEIC certificate)'
  }
]

const education = [
  {
    title: "Master's Degree in Computer Science and Engineering",
    institution: 'Politecnico di Milano',
    period: 'Sep 2021 - Apr 2025',
    grade: 'Final grade: 110/110 cum laude'
  },
  {
    title: "Bachelor's Degree in Computer Engineering",
    institution: 'Politecnico di Milano',
    period: 'Sep 2018 - Sep 2021',
    grade: 'Final grade: 103/110'
  },
  {
    title: 'Traditional Scientific High School',
    institution: 'Alessandro Volta (Milan)',
    period: 'Sep 2013 - Jun 2018',
    grade: 'Final grade: 96/100'
  }
]

const projects = [
  {
    title: "Master's Thesis: Reinforcement Learning for Digital Advertising Cross-Channel Budget Optimization",
    description: 'The thesis explores the use of Reinforcement Learning algorithms to optimize conversions generated by digital advertising campaigns, efficiently distributing the available budget across multiple advertising channels. The main challenge is modeling the advertising environment through a simulator capable of generating structured data according to a Markov Decision Process.',
    achievement: null
  },
  {
    title: 'Software Engineering Project in the SCORE Competition',
    description: 'The project involves extending the CodeDefenders website, a platform that organizes games to improve testing skills. The goal is to develop a new website that, integrating with the CodeDefenders API, enables the organization of tournaments for these games. The final application is designed to support load balancing by leveraging multiple CodeDefenders servers. This work achieved second place in the SCORE competition in 2023.',
    achievement: '2nd Place SCORE 2023'
  },
  {
    title: 'Videogame Design and Development Project',
    description: 'Videogame developed in C# with Unity in the context of the Video Game Design and Development university course.',
    achievement: null
  },
  {
    title: 'Web development Course Project',
    description: 'A web application for university exam management for both professors and students, developed with Java Enterprise Edition.',
    achievement: null
  },
  {
    title: 'Distributed Systems Project',
    description: 'Implementation and simulation of the Raft protocol using the C++ Omnet library.',
    achievement: null
  },
  {
    title: 'Deep Learning Project',
    description: 'Use of Neural Networks for plant recognition from images and classification of multivariate time series within the university Deep Learning competition.',
    achievement: null
  },
  {
    title: 'Text Editor Developed in C',
    description: 'The main focus of this project was the optimization of memory and speed.',
    achievement: null
  },
  {
    title: 'Data Mining Portfolio',
    description: 'Portfolio that includes different implementations of data mining algorithms.',
    achievement: null
  }
]

const getSkillIcon = (index: number) => {
  const icons = ['💻', '🗄️', '⚙️', '🔧', '🤖', '🌐']
  return icons[index] || '📋'
}
</script>