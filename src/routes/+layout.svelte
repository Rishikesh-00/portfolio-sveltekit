<script>
    import "../app.css";
    import Contact from "../lib/components/Contact.svelte";
    import Education from "../lib/components/Education.svelte";
    import Hero from "../lib/components/Hero.svelte";
    import Navbar from "../lib/components/Navbar.svelte";
    import Projects from "../lib/components/Projects.svelte";
    import Skills from "../lib/components/Skills.svelte";
    import SocialLinks from "../lib/components/SocialLinks.svelte";
    import Test from "../lib/components/test.svelte";
  </script>
  <Navbar/>
  <SocialLinks/>
  <Hero/>
  <Education/>
  <Projects/>
  <Skills></Skills>
  <Contact></Contact>
  <!-- <Test></Test> -->
  <slot />