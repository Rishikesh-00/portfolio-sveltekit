<script>
    import { onMount } from 'svelte';
    import AOS from 'aos';
    import 'aos/dist/aos.css';
  
    // Import images
    import Html from '../assets/html.png';
    import Css from '../assets/css.png';
    import Js from '../assets/js.png';
    import Jquerry from '../assets/jquerry.png';
    import Sveltekit from '../assets/SvelteKit.png';
    import Node from '../assets/node.png';
    import Express from '../assets/express1.png';
    import MongoDb from '../assets/mongodb.png';
    import Mysql from '../assets/mysql.png';
    import Github from '../assets/github.png';
    import Tailwind from '../assets/tailwind.png';
    import Java from '../assets/java.png';
  
    // Techs array
    const techs = [
      { id: 11, src: Java, title: 'Java', shadow: 'shadow-orange-500' },
      { id: 1, src: Html, title: 'HTML', shadow: 'shadow-orange-500' },
      { id: 2, src: Css, title: 'CSS', shadow: 'shadow-blue-500' },
      { id: 3, src: Js, title: 'JavaScript', shadow: 'shadow-yellow-500' },
      { id: 4, src: Jquerry, title: 'JQuerry', shadow: 'shadow-blue-500' },
      { id: 5, src: Sveltekit, title: 'Sveltekit', shadow: 'shadow-orange-500' },
      { id: 6, src: Express, title: 'Express', shadow: 'shadow-white' },
      { id: 7, src: Node, title: 'Node', shadow: 'shadow-green-400' },
      // { id: 8, src: MongoDb, title: 'MongoDB', shadow: 'shadow-green-400' },
      { id: 9, src: Tailwind, title: 'Tailwind', shadow: 'shadow-sky-400' },
      { id: 10, src: Mysql, title: 'MySQL', shadow: 'shadow-blue-400' },
      { id: 11, src: Github, title: 'Git & GitHub', shadow: 'shadow-gray-400' },
      
    ];
  
    onMount(() => {
      AOS.init({ duration: 1000 });
    });
  </script>
  
  <div id="skills" class="bg-gradient-to-b from-gray-800 to-black w-full h-full">
    <div class="max-w-screen-lg mx-auto p-4 flex flex-col justify-center w-full h-full text-white">
      <div>
        <p class="text-4xl font-bold border-b-4 border-gray-500 p-2 inline-block" data-aos="fade-in" data-aos-duration="800">Skills</p>
        <p class="py-6" data-aos="fade-in" data-aos-duration="1000">These are the technologies I've worked with</p>
      </div>
  
      <div class="w-full grid grid-cols-2 sm:grid-cols-3 gap-8 text-center py-8 px-12 sm:px-0">
        {#each techs as { id, src, title, shadow }}
          <div key={id} data-aos="zoom-in" data-aos-duration="500" class={`shadow-md hover:scale-105 duration-500 py-2 rounded-lg ${shadow}`}>
            <img src={src} alt={title} class="w-20 mx-auto" />
            <p class="mt-4">{title}</p>
          </div>
        {/each}
      </div>
    </div>
  </div>
  