<script>
    import { onMount } from 'svelte';
    import AOS from 'aos';
    import 'aos/dist/aos.css';
  
    onMount(() => {
      AOS.init({ duration: 1000 });
    });
  </script>
  
  <div id="contact" class="bg-gradient-to-b from-black to-gray-800 p-4 text-white">
    <div class="max-w-screen-lg mx-auto">
      <div class="pb-8">
        <p class="text-4xl font-bold inline border-b-4 border-gray-500" data-aos="fade-in" data-aos-duration="800">Contact</p>
        <p class="py-6" data-aos="fade-in" data-aos-duration="1000">Submit the form below to get in touch with me</p>
      </div>
  
      <div class="flex justify-center items-center">
        <form action="https://getform.io/f/mepEwXaM" method="POST" class="flex flex-col w-full md:w-1/2">
          <input type="text" data-aos="slide-up" data-aos-duration="500" name="name" id="nam" placeholder="Enter your name" class="p-2 bg-transparent border-2 rounded-md text-white focus:outline-none" required />
          
          <input type="email" data-aos="slide-up" data-aos-duration="700" name="email" placeholder="Enter your email" class="my-4 p-2 bg-transparent border-2 rounded-md text-white focus:outline-none" id="mail" required />
          
          <textarea name="message" data-aos="fade-in" data-aos-duration="900" id="msg" rows="10" required class="p-2 bg-transparent border-2 rounded-md text-white focus:outline-none" placeholder="Enter your message"></textarea>
  
          <button type="submit" class="text-white bg-gradient-to-b from-cyan-500 to-blue-500 px-6 py-3 my-8 mx-auto items-center rounded-md hover:scale-110 duration-300"><b>Let's talk</b></button>
        </form>
      </div>
    </div>
  </div>
  