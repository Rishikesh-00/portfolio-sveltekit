<!-- Navbar.svelte -->
<script>
    import { onMount } from "svelte";
  
    let nav = false;
  
    const links = [
      { id: 1, link: "home" },
      { id: 2, link: "education" },
      { id: 3, link: "project" },
      { id: 4, link: "skills" },
      { id: 5, link: "contact" },
    ];
  
    function toggleNav() {
      nav = !nav;
    }
  
    function smoothScroll(link) {
      document.getElementById(link)?.scrollIntoView({
        behavior: "smooth",
      });
      nav = false;
    }
  </script>
  
  <div class="flex justify-between items-center w-full h-16 text-white fixed bg-black px-4 z-10">
    <div>
      <h1 class="text-5xl font-signature ml-2">Rishi</h1>
    </div>
  
    <!-- Desktop Links -->
    <ul class="hidden md:flex">
      {#each links as { id, link }}
        <li
          key={id}
          class="px-4 cursor-pointer capitalize font-medium text-gray-500 hover:scale-105 duration-200"
          on:click={() => smoothScroll(link)}
        >
          {link}
        </li>
      {/each}
    </ul>
  
    <!-- Mobile Menu Icon -->
    <div class="cursor-pointer pr-4 z-10 text-gray-500 md:hidden" on:click={toggleNav}>
      {#if nav}
        <i class='bx bx-x text-4xl'></i>
      {:else}
        <i class='bx bx-menu-alt-left text-4xl'></i>
      {/if}
    </div>
  
    <!-- Mobile Links -->
    {#if nav}
      <ul class="flex flex-col justify-center items-center absolute top-0 left-0 w-full h-screen bg-gradient-to-b from-black to-gray-500">
        {#each links as { id, link }}
          <li
            key={id}
            class="px-4 py-6 cursor-pointer capitalize text-2xl"
            on:click={() => smoothScroll(link)}
          >
            {link}
          </li>
        {/each}
      </ul>
    {/if}
  </div>
  
  <!-- Main content of the page -->
  
  