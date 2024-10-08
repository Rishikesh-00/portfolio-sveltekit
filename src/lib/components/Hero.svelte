<script>
  import AOS from "aos";
  import "aos/dist/aos.css";
  import { onMount } from "svelte";
  import MyImage from "../assets/pro.jpeg";
  import Resume from "../assets/Rishikesh_resume.pdf";
  onMount(() => {
    AOS.init({ duration: 1000 });
  });
</script>

<div
  id="home"
  class="h-screen w-full bg-gradient-to-b from-black via-black to-gray-800"
>
  <div
    class="max-w-screen-lg mx-auto flex flex-col items-center justify-center h-full px-4 md:flex-row"
  >
    <div class="flex flex-col justify-center h-full">
      <h2
        class="text-4xl sm:text-7xl font-bold text-white"
        data-aos="fade-out"
        data-aos-duration="1500"
      >
        I'm a Full Stack Developer
      </h2>
      <p
        class="text-gray-500 py-4 max-w-md"
        data-aos="slide-up"
        data-aos-duration="500"
      >
        Hey, my name is Rishikesh. Currently, I am pursuing MCA. I love to work
        on applications using technologies like Svelte, Tailwind CSS, Nodejs,
        and MySQL.
      </p>
      <div class="flex">
        <a
          href="#portfolio"
          class="text-white w-fit px-6 py-3 my-2 flex items-center rounded-md bg-gradient-to-r from-cyan-500 to-blue-500 cursor-pointer group"
          data-aos="slide-up"
          data-aos-duration="500"
        >
          Portfolio
          <span class="group-hover:rotate-90 duration-300">
            <i class="bx bxs-chevron-right ml-1 text-2xl"></i>
          </span>
        </a>
        <div class="m-3">
          <a
            href={Resume}
            download="resume.pdf"
            class="bg-white text-gray-800 font-bold rounded border-b-2 border-green-500 hover:border-green-600 hover:bg-green-500 transition-all duration-300 hover:text-white shadow-md py-2 px-6 inline-flex items-center"
            data-aos="slide-up"
            data-aos-duration="500"
          >
            <span class="mr-2">Download Resume</span>

            <i class="bx bx-download text-2xl"></i>
          </a>
        </div>
      </div>
    </div>
    <div>
      <img
        src={MyImage}
        alt="profile"
        class="h-30 rounded-2xl mx-auto w-1/3 md:w-80"
      />
    </div>
  </div>
</div>

<style>
  /* Add any custom CSS styles if needed */
</style>
