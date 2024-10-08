
<script>
  import { onMount } from "svelte";
  import FrontendProject from './FrontendProject.svelte';
  import FullStackProject from './FullStackProject.svelte';
  import DesktopProject from './DesktopProject.svelte';

  let activeTab = 0; // Index of the active tab
  let tabs = ["Frontend", "Full-Stack", "Desktop"]; // Tab labels
  let barWidth = "0px"; // Width of the bar
  let barOffset = "0px"; // Offset for the bar

  onMount(() => {
    const tabsWrapper = document.querySelector(".tabs-wrapper");
    const activeTabElement = tabsWrapper.children[activeTab];
    barWidth = `${activeTabElement.offsetWidth}px`;
    barOffset = `${activeTabElement.offsetLeft}px`;
  });

  const changeSelected = (index) => {
    activeTab = index;
    const tabsWrapper = document.querySelector(".tabs-wrapper");
    const activeTabElement = tabsWrapper.children[activeTab];
    barWidth = `${activeTabElement.offsetWidth}px`;
    barOffset = `${activeTabElement.offsetLeft}px`;
  };
</script>
<div id="project" class="bg-gradient-to-b from-black to-gray-800 w-full h-full">
  <div class="max-w-screen-lg mx-auto p-4 flex flex-col justify-center w-full h-full text-white">
    <div>
      <p class="text-4xl font-bold border-b-4 border-gray-500 p-2 inline-block" data-aos="fade-in" data-aos-duration="800">Projects</p>
      <p class="py-6" data-aos="fade-in" data-aos-duration="1000">These are my latest projects</p>
    </div>
<!-- <div name="portfolio" class="bg-gradient-to-b from-black to-gray-800 w-full text-white  pt-10"> -->
  
  <div id="project" class="container flex justify-center items-center">
    <nav class="tabs-wrapper" style="--bar-width: {barWidth}; --bar-offset: {barOffset}">
      {#each tabs as tab, index}
        <div class="tab" on:click={() => changeSelected(index)} tabindex="0">
          {tab}
        </div>
      {/each}
    </nav>
  </div>

  <!-- Conditionally render the selected component -->
  <div class="mt-8">
    {#if activeTab === 0}
      <FrontendProject />
    {:else if activeTab === 1}
      <FullStackProject />
    {:else if activeTab === 2}
      <DesktopProject />
    {/if}
  </div>
</div>
</div>
<!-- </div> -->

<style>
  /* Component */
  .tabs-wrapper {
    --_bar_height: 4px;
    --_bar-color: #f1f1f1;
    --_bar-background-opacity: 0.2;

    --_transition-time: 0.2s; /* Transition of the bar (width and transform) */

    --_text-color: var(--_bar-color);
    --_font-size: 18px;

    position: relative;
    display: inline-flex;
    flex-direction: row;
    padding-bottom: var(--_bar_height);
  }
  .tabs-wrapper::before,
  .tabs-wrapper::after {
    position: absolute;
    bottom: 0;
    content: "";
    height: var(--_bar_height);
    width: 100%;
    background: var(--_bar-color);
    opacity: var(--_bar-background-opacity);
    border-radius: var(--_bar_height);
  }
  .tabs-wrapper::after {
    width: var(--bar-width);
    opacity: 1;
    transform: translateX(var(--bar-offset));
    transition:
      width var(--_transition-time) ease,
      transform var(--_transition-time) ease;
  }
  .tabs-wrapper .tab {
    padding: 0.5rem 2rem;
    font-family: Arial;
    font-size: var(--_font-size);
    color: var(--_text-color);
    cursor: pointer;
    user-select: none;
  }
  /* .tabs-wrapper .tab:focus-visible { 
    background: rgba(0, 0, 0, 0.2);
    outline: none;
    border-radius: 5px 5px 0 0;
  } */
</style>
