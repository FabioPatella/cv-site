<template>
  <div class="min-h-screen bg-gray-50">
    <!-- Navigazione -->
    <nav class="fixed top-0 w-full bg-white/90 backdrop-blur-md border-b border-gray-200 z-50 shadow-sm">
      <div class="container mx-auto px-6 py-4">
        <div class="flex items-center justify-between">
          <h1 class="text-xl font-bold text-gray-900 hidden md:block">Fabio Patella</h1>
          <div class="flex flex-wrap gap-x-6 gap-y-2 w-full md:w-auto md:ml-8">
            <a href="#about" :class="linkClass('about')" @click.prevent="handleNavClick('about')">Chi sono</a>
            <a href="#experience" :class="linkClass('experience')" @click.prevent="handleNavClick('experience')">Esperienza</a>
            <a href="#education" :class="linkClass('education')" @click.prevent="handleNavClick('education')">Formazione</a>
            <a href="#skills" :class="linkClass('skills')" @click.prevent="handleNavClick('skills')">Competenze</a>
            <a href="#projects" :class="linkClass('projects')" @click.prevent="handleNavClick('projects')">Progetti</a>
            <a href="#contact" :class="linkClass('contact')" @click.prevent="handleNavClick('contact')">Contatti</a>
            <div class="flex items-center gap-1 text-sm font-medium">
  <a href="/" class="text-gray-400 hover:text-gray-700 transition-colors">EN</a>
  <span class="text-gray-300">|</span>
  <a href="/it" class="text-blue-600 underline underline-offset-4 font-semibold">IT</a>
</div>
          </div>
        </div>
      </div>
    </nav>

    <!-- Hero -->
    <section id="about" class="pt-32 pb-16 px-6 bg-gray-50 scroll-mt-24">
      <div class="container mx-auto max-w-4xl">
        <div class="grid md:grid-cols-3 gap-12 items-center">
          <div class="md:col-span-2">
            <div class="inline-block bg-blue-100 text-blue-700 px-4 py-2 rounded-full text-sm font-medium mb-6">
              Ingegnere del Software
            </div>
            <h2 class="text-5xl md:text-6xl font-bold text-gray-900 mb-6">
              Fabio Patella
            </h2>
            <p class="text-lg text-gray-700 mb-8 leading-relaxed">
              Neolaureato in Ingegneria Informatica al Politecnico di Milano, con competenze trasversali nell'informatica e specializzazione in ingegneria del software. Residente a Milano.
            </p>
            <div class="flex flex-wrap gap-4">
              <a href="mailto:fabio140199@gmail.com?subject=Richiesta%20dal%20sito%20CV" class="bg-blue-600 text-white px-8 py-3 rounded-lg font-medium hover:bg-blue-700 transition shadow-lg shadow-blue-600/30">
                Contattami
              </a>
              <a href="https://linkedin.com/in/fabio-patella" target="_blank" class="bg-white text-gray-900 px-8 py-3 rounded-lg font-medium hover:bg-gray-50 transition shadow-md border border-gray-200">
                LinkedIn
              </a>
            </div>
          </div>
          <div class="flex justify-center md:justify-end">
            <img src="/static/images/profile.png" alt="Fabio Patella" class="w-56 h-56 rounded-full object-cover border-4 border-blue-200 shadow-lg" />
          </div>
        </div>
      </div>
    </section>

    <!-- Esperienza -->
    <section id="experience" class="py-16 px-6 bg-gray-50 scroll-mt-24">
      <div class="container mx-auto max-w-4xl">
        <div class="text-center mb-16">
          <h3 class="text-4xl font-bold text-gray-900 mb-4">Esperienze lavorative</h3>
          <p class="text-gray-600 text-lg">Percorso professionale e responsabilità</p>
        </div>
        
        <div class="max-w-3xl mx-auto">
          <div class="bg-gradient-to-br from-white to-gray-50 p-8 rounded-xl border border-gray-200 shadow-md hover:shadow-xl transition">
            <div class="flex justify-between items-start mb-4">
              <div>
                <h4 class="text-2xl font-bold text-gray-900 mb-2">Sviluppatore Fullstack &amp; Manutenzione Applicativa</h4>
                <p class="text-blue-700 font-semibold text-lg">Tamtamy Reply</p>
              </div>
              <span class="text-sm text-gray-500 bg-gray-100 px-4 py-2 rounded-full font-medium whitespace-nowrap">Da Giu 2025</span>
            </div>
            
            <div class="space-y-4 mt-6">
              <div class="flex items-start gap-3">
                <div class="w-2 h-2 bg-blue-600 rounded-full mt-2 flex-shrink-0"></div>
                <div>
                  <p class="text-gray-700 font-medium mb-1">Sviluppo Fullstack (50%)</p>
                  <p class="text-gray-600 text-sm">Sviluppo frontend con Vue.js (25%) e backend con Laravel (25%)</p>
                </div>
              </div>
              <div class="flex items-start gap-3">
                <div class="w-2 h-2 bg-blue-600 rounded-full mt-2 flex-shrink-0"></div>
                <div>
                  <p class="text-gray-700 font-medium mb-1">Manutenzione Applicativa (50%)</p>
                  <p class="text-gray-600 text-sm">Manutenzione e miglioramento di applicazioni esistenti, bug fixing e ottimizzazione delle prestazioni</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Formazione -->
    <section id="education" class="py-16 px-6 bg-gray-50 scroll-mt-24">
      <div class="container mx-auto max-w-4xl">
        <div class="text-center mb-16">
          <h3 class="text-4xl font-bold text-gray-900 mb-4">Formazione</h3>
          <p class="text-gray-600 text-lg">Percorso accademico e qualifiche</p>
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

    <!-- Competenze -->
    <section id="skills" class="py-16 px-6 scroll-mt-24">
      <div class="container mx-auto max-w-4xl">
        <div class="text-center mb-16">
          <h3 class="text-4xl font-bold text-gray-900 mb-4">Competenze Tecniche</h3>
          <p class="text-gray-600 text-lg">Competenze chiave ed esperienza tecnica</p>
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

    <!-- Progetti -->
    <section id="projects" class="py-16 px-6 scroll-mt-24">
      <div class="container mx-auto max-w-4xl">
        <div class="text-center mb-16">
          <h3 class="text-4xl font-bold text-gray-900 mb-4">Progetti in Evidenza</h3>
        <p class="text-gray-600 text-lg">Esperienze selezionate di lavoro e ricerca</p>
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

    <!-- Contatti -->
    <section id="contact" class="py-16 px-6 scroll-mt-24">
      <div class="container mx-auto max-w-4xl">
        <div class="text-center mb-16">
          <h3 class="text-4xl font-bold text-gray-900 mb-4">Restiamo in Contatto</h3>
          <p class="text-gray-600 text-lg">Scrivimi per opportunità o collaborazioni</p>
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
              <svg viewBox="0 0 24 24" aria-hidden="true" class="w-8 h-8 fill-white">
                <path d="M4.98 3.5C4.98 4.88 3.86 6 2.5 6S0 4.88 0 3.5 1.12 1 2.5 1s2.48 1.12 2.48 2.5zM0 8.16h5V24H0V8.16zM8.98 8.16h4.78v2.16h.07c.66-1.25 2.27-2.57 4.68-2.57 5 0 5.92 3.29 5.92 7.57V24h-5v-6.93c0-1.65-.03-3.77-2.3-3.77-2.3 0-2.65 1.8-2.65 3.65V24h-5V8.16z"/>
              </svg>
            </div>
            <p class="text-xs text-gray-500 uppercase font-semibold tracking-wide mb-2">LinkedIn</p>
            <p class="text-gray-900 font-semibold">fabio-patella</p>
          </a>
          <a href="https://github.com/FabioPatella" target="_blank" class="bg-gradient-to-br from-blue-50 to-indigo-50 p-8 rounded-xl border border-blue-200 hover:border-blue-400 hover:shadow-xl transition group text-center">
            <div class="w-16 h-16 bg-blue-600 rounded-full flex items-center justify-center mx-auto mb-4 group-hover:scale-110 transition">
              <svg viewBox="0 0 24 24" aria-hidden="true" class="w-8 h-8 fill-white">
                <path d="M12 .5a11.5 11.5 0 0 0-3.64 22.41c.58.11.79-.25.79-.56v-2c-3.22.7-3.9-1.4-3.9-1.4-.53-1.36-1.3-1.72-1.3-1.72-1.06-.72.08-.71.08-.71 1.18.08 1.8 1.22 1.8 1.22 1.04 1.79 2.73 1.27 3.4.97.11-.76.41-1.27.75-1.56-2.57-.29-5.28-1.28-5.28-5.7 0-1.26.45-2.29 1.2-3.1-.12-.3-.52-1.52.11-3.18 0 0 .98-.31 3.2 1.18a11.1 11.1 0 0 1 5.82 0c2.22-1.49 3.2-1.18 3.2-1.18.63 1.66.23 2.88.11 3.18.75.81 1.2 1.84 1.2 3.1 0 4.43-2.71 5.4-5.29 5.69.42.36.8 1.07.8 2.17v3.22c0 .31.21.68.8.56A11.5 11.5 0 0 0 12 .5Z"/>
              </svg>
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
        <p class="text-gray-600">&copy; 2025 Fabio Patella. Tutti i diritti riservati.</p>
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

// Seleziona la sezione attiva più vicina al centro viewport
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
    title: 'Linguaggi di Programmazione',
    description: 'C, C++, C#, Java, JavaScript, Python, PHP'
  },
  {
    title: 'Competenze Database',
    description: 'Progettazione concettuale e logica, integrazione e gestione di database distribuiti, interrogazione con SQL e MySQL, uso della libreria JPA per Object/Relational Mapping'
  },
  {
    title: 'Framework di Programmazione',
    description: 'Java Enterprise Edition, Java Spring e Laravel per il backend, React e Vue per lo sviluppo Front-End. Tecnologie per sistemi distribuiti: MPI, Node-Red, Akka, Spark'
  },
  {
    title: 'Strumenti per il Processo Software',
    description: 'Git/GitHub, Docker, testing (JUnit, PyTest, Mockito), specifica, verifica, validazione e progettazione del software (Alloy, Uppaal), pratiche Agile (SCRUM)'
  },
  {
    title: 'Intelligenza Artificiale',
    description: 'Machine Learning e Data Mining (Scikit-Learn), Deep Learning (TensorFlow, Keras), Reinforcement Learning (Stable-Baselines3)'
  },
  {
    title: 'Lingue',
    description: 'Italiano (madrelingua), Inglese livello B2 (certificati First e TOEIC)'
  }
]

const education = [
  {
    title: 'Laurea Magistrale in Ingegneria Informatica',
    institution: 'Politecnico di Milano',
    period: 'Set 2021 - Apr 2025',
    grade: 'Voto finale: 110/110 e lode'
  },
  {
    title: 'Laurea Triennale in Ingegneria Informatica',
    institution: 'Politecnico di Milano',
    period: 'Set 2018 - Set 2021',
    grade: 'Voto finale: 103/110'
  },
  {
    title: 'Liceo Scientifico Tradizionale',
    institution: 'Alessandro Volta (Milano)',
    period: 'Set 2013 - Giu 2018',
    grade: 'Voto finale: 96/100'
  }
]

const projects = [
  {
    title: 'Tesi Magistrale: Reinforcement Learning per l\'Ottimizzazione del Budget Pubblicitario Cross-Channel',
    description: 'La tesi esplora l\'uso di algoritmi di Reinforcement Learning per ottimizzare le conversioni generate da campagne di advertising digitale, distribuendo in modo efficiente il budget disponibile tra più canali pubblicitari. La sfida principale è modellare l\'ambiente pubblicitario tramite un simulatore capace di generare dati strutturati secondo un Markov Decision Process.',
    achievement: null
  },
  {
    title: 'Progetto di Ingegneria del Software nella Competizione SCORE',
    description: 'Il progetto prevede l\'estensione del sito CodeDefenders, una piattaforma che organizza giochi per migliorare le competenze di testing. L\'obiettivo è sviluppare un nuovo sito che, integrandosi con le API di CodeDefenders, consenta l\'organizzazione di tornei per questi giochi. L\'applicazione finale supporta il bilanciamento del carico sfruttando più server CodeDefenders. Questo lavoro ha raggiunto il secondo posto alla competizione SCORE nel 2023.',
    achievement: '2° posto SCORE 2023'
  },
  {
    title: 'Progetto di Progettazione e Sviluppo Videogiochi',
    description: 'Videogioco sviluppato in C# con Unity nel contesto del corso universitario di Video Game Design and Development.',
    achievement: null
  },
  {
    title: 'Progetto del Corso di Sviluppo Web',
    description: 'Applicazione web per la gestione degli esami universitari per docenti e studenti, sviluppata con Java Enterprise Edition.',
    achievement: null
  },
  {
    title: 'Progetto di Sistemi Distribuiti',
    description: 'Implementazione e simulazione del protocollo Raft utilizzando la libreria Omnet in C++.',
    achievement: null
  },
  {
    title: 'Progetto di Deep Learning',
    description: 'Uso di Reti Neurali per il riconoscimento delle piante da immagini e la classificazione di serie temporali multivariate all\'interno della competizione universitaria di Deep Learning.',
    achievement: null
  },
  {
    title: 'Editor di Testo Sviluppato in C',
    description: 'Focus principale su ottimizzazione della memoria e delle prestazioni.',
    achievement: null
  },
  {
    title: 'Portfolio di Data Mining',
    description: 'Portfolio che include diverse implementazioni di algoritmi di data mining.',
    achievement: null
  }
]

const getSkillIcon = (index: number) => {
  const icons = ['💻', '🗄️', '⚙️', '🔧', '🤖', '🌐']
  return icons[index] || '📋'
}
</script>

