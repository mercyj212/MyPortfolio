
<template>
  <Navbar />

  <!-- Home -->
  <Hero class="animate-section"/>


  <!-- Projects -->
  <Projects class="animate-section" />

  <!-- About -->
   <About class="animate-section"/>
 

  <!-- Contact -->
   <Contact class="animate-section"/>
  
</template>


<script setup>
  import Hero from './components/Hero.vue';
  import Navbar from './components/Navbar.vue'
  import Projects from './components/Projects.vue';
  import About from './components/About.vue';
  import Contact from './components/Contact.vue';


    import { onMounted } from 'vue';
    import gsap from 'gsap'
    import { ScrollTrigger } from 'gsap/ScrollTrigger'; 
    
    gsap.registerPlugin(ScrollTrigger)

    onMounted(() => {
       const sections = gsap.utils.toArray(".animate-section")

       sections.forEach((section) => {
        gsap.fromTo(
            section,
            { y: 100, opacity: 0 },
            {
                y: 0,
                opacity: 1,
                duration: 1.2,
                ease: "power3.out",
                scrollTrigger: {
                    trigger: section,
                    start: "top 80%",
                    end: "bottom 20%",
                    toggleActions: "restart none restart none"
                }
            }
        )
      })
    })
</script>  
