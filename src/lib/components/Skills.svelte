<script>
    import { onMount } from 'svelte';
    import AOS from 'aos';
    import 'aos/dist/aos.css';
  
    // Import images
    import Html from '../assets/html.png';
    import Css from '../assets/css.png';
    import Js from '../assets/js.png';
    import React from '../assets/react.png';
    import NextJs from '../assets/nextjs.svg';
    import Typescript from '../assets/typescript.svg';
    import Redux from '../assets/redux.svg';
    import Tanstack from '../assets/reactquery.svg';
    import Tailwind from '../assets/tailwind.png';
    import Shadcn from '../assets/shadcnui.svg';
    import Node from '../assets/node.png';
    import Express from '../assets/express1.png';
    import Jwt from '../assets/jwt.svg';
    import Socketio from '../assets/socketio.svg';
    import Mysql from '../assets/mysql.png';
    import Firebase from '../assets/firebase.svg';
    import Git from '../assets/git.svg';
    import Github from '../assets/github.png';
    import Postman from '../assets/postman.svg';
    import Vscode from '../assets/vscode.svg';
  
    // Techs grouped by category
    const categories = [
      {
        title: 'Frontend',
        techs: [
          { id: 1, src: React, title: 'React.js', shadow: 'shadow-cyan-400' },
          { id: 2, src: NextJs, title: 'Next.js', shadow: 'shadow-gray-400' },
          { id: 3, src: Typescript, title: 'TypeScript', shadow: 'shadow-blue-600' },
          { id: 4, src: Js, title: 'JavaScript (ES6+)', shadow: 'shadow-yellow-500' },
          { id: 5, src: Redux, title: 'Redux Toolkit', shadow: 'shadow-purple-500' },
          { id: 6, src: Tanstack, title: 'TanStack Query', shadow: 'shadow-red-400' },
          { id: 7, src: Tailwind, title: 'Tailwind CSS', shadow: 'shadow-sky-400' },
          { id: 8, src: Shadcn, title: 'ShadCN UI', shadow: 'shadow-gray-400' },
          { id: 9, src: Html, title: 'HTML5', shadow: 'shadow-orange-500' },
          { id: 10, src: Css, title: 'CSS3', shadow: 'shadow-blue-500' },
        ],
      },
      {
        title: 'Backend',
        techs: [
          { id: 11, src: Node, title: 'Node.js', shadow: 'shadow-green-400' },
          { id: 12, src: Express, title: 'Express.js', shadow: 'shadow-white' },
          { id: 13, icon: 'bx bx-transfer-alt', title: 'REST APIs', shadow: 'shadow-emerald-400' },
          { id: 14, src: Jwt, title: 'JWT Authentication', shadow: 'shadow-pink-500' },
          { id: 15, src: Socketio, title: 'Socket.IO', shadow: 'shadow-gray-400' },
        ],
      },
      {
        title: 'Database',
        techs: [
          { id: 16, src: Mysql, title: 'MySQL', shadow: 'shadow-blue-400' },
          { id: 17, src: Firebase, title: 'Firebase', shadow: 'shadow-amber-500' },
        ],
      },
      {
        title: 'Tools',
        techs: [
          { id: 18, src: Git, title: 'Git', shadow: 'shadow-orange-600' },
          { id: 19, src: Github, title: 'GitHub', shadow: 'shadow-gray-400' },
          { id: 20, src: Postman, title: 'Postman', shadow: 'shadow-orange-500' },
          { id: 21, src: Vscode, title: 'VS Code', shadow: 'shadow-blue-500' },
        ],
      },
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
  
      {#each categories as { title, techs }}
        <div class="pt-2 pb-6">
          <h3 class="text-xl font-semibold text-emerald-500 pb-4 uppercase tracking-wide" data-aos="fade-in" data-aos-duration="800">
            {title}
          </h3>
          <div class="w-full grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 lg:grid-cols-5 gap-8 text-center py-4 px-12 sm:px-0">
            {#each techs as { id, src, icon, title, shadow }}
              <div key={id} data-aos="zoom-in" data-aos-duration="500" class={`shadow-md hover:scale-105 duration-500 py-2 rounded-lg ${shadow}`}>
                {#if icon}
                  <i class={`${icon} text-[80px] mx-auto flex justify-center text-white leading-none`}></i>
                {:else}
                  <img src={src} alt={title} class="w-20 mx-auto" />
                {/if}
                <p class="mt-4">{title}</p>
              </div>
            {/each}
          </div>
        </div>
      {/each}
    </div>
  </div>
  