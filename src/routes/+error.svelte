<script>
    import { onMount } from 'svelte';
  
    let currentTheme = 'light';
  
    // Function to toggle theme color
    function toggleTheme() {
      const root = document.documentElement;
  
      if (currentTheme === 'dark') {
        root.style.setProperty('--bg-color', '#fff');
        root.style.setProperty('--text-color', '#000');
        currentTheme = 'light';
      } else {
        root.style.setProperty('--bg-color', '#050505');
        root.style.setProperty('--text-color', '#fff');
        currentTheme = 'dark';
      }
    }
  
    onMount(() => {
      // Set initial theme icon based on currentTheme
      document.documentElement.style.setProperty('--bg-color', currentTheme === 'dark' ? '#050505' : '#fff');
      document.documentElement.style.setProperty('--text-color', currentTheme === 'dark' ? '#fff' : '#000');
    });
  </script>
  
  <button
    class="color-switcher"
    on:click={toggleTheme}
    aria-label="Toggle theme color"
    title="Toggle theme color">
    {currentTheme === 'dark' ? '🌞' : '🌙'}
  </button>
  
  <style>
    .color-switcher {
      position: fixed;
      top: 40px;
      right: 40px;
      background-color: transparent;
      font-size: var(--fs-icon);
      cursor: pointer;
      color: var(--primary-color);
      border: 0;
    }
  </style>
  