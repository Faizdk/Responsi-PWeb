<template>
    <link rel='stylesheet' href='https://cdn.jsdelivr.net/npm/bootstrap@4.4.1/dist/css/bootstrap.min.css'>
   <div>
     <ContactSection />
   </div>
       <!-- Menambahkan Navbar (in)-->
       <nav>
       <section class="nav">
             <a><NuxtLink to="/" class="nav-item">Home</NuxtLink></a>
             <a><NuxtLink to="/about" class="nav-item">About</NuxtLink></a>
             <a><NuxtLink to="/project" class="nav-item">Project</NuxtLink></a>
             <a><NuxtLink to="/contact" class="nav-item">Contact</NuxtLink></a>
       </section>
     </nav>
     <!-- Menambahkan Navbar (end)-->
  </template>
  
  <script>
  import HeroSection from '~/components/HeroSection.vue';
  import AboutSection from '~/components/AboutSection.vue';
  import ProjectsSection from '~/components/ProjectsSection.vue';
  import ContactSection from '~/components/ContactSection.vue';
  
  export default {
   components: {
     ContactSection,
   }
  }
  </script>./contact.vue