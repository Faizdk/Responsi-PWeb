<template>
  <div>
    <HeroSection />
  </div>
  <nav>
       <section class="nav">
             <a><NuxtLink to="/" class="nav-item">Home</NuxtLink></a>
             <a><NuxtLink to="/about" class="nav-item">About</NuxtLink></a>
             <a><NuxtLink to="/project" class="nav-item">Project</NuxtLink></a>
             <a><NuxtLink to="/contact" class="nav-item">Contact</NuxtLink></a>
       </section>
     </nav>
</template>

<script>
import HeroSection from '~/components/HeroSection.vue';
import AboutSection from '~/components/AboutSection.vue';
import ProjectsSection from '~/components/ProjectsSection.vue';
import ContactSection from '~/components/ContactSection.vue';

export default {
  components: {
    HeroSection,
  }
}
</script>./Index.vue
