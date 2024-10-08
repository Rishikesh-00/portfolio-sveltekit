<script>
  // import Desktop from "$lib/projectImages/desktop/desktop.jpeg"
    const portfolioList = [
      {
        image: "./projectImages/Desktop/desktop.jpeg",
        title: "Branding",
        description:
          "Sed ut in perspiciatis unde omnis iste natus error sit on i tatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae.",
        href:"https://zelt-clone-by-rishi.netlify.app/",
        git:"https://github.com/Rishikesh-00/Institute_Management_System.git",
      },
      // {
      //   image: Astra,
      //   title: "Marketing",
      //   description:
      //     "It’s easier to reach your savings goals when you have the right savings account. It’s easier to reach your savings goals when you have the right savings account.",
      //     href:"https://afina-clone.netlify.app/",
      //     git:"",
      // },
      // {
      //   image: Hosterr,
      //   title: "Development",
      //   description:
      //     "Vitae bibendum egestas magna sit elit non. Netus volutpat dignissim pharetra felis. Orci commodo mauris digital industry is booming adipiscing semper amet.",
      //   href:"https://hosterr-clone.netlify.app/",
      //   git:"",
      // },
    ];
  </script>
  
  <section class="text-white">
    <div class="container px-4 mx-auto">
      
  
      <div class="grid grid-cols-6 gap-6 gap-y-8 lg:gap-y-0 max-w-7xl mx-auto">
        {#each portfolioList as portfolio, i}
          <div class="col-span-6 md:col-span-3 lg:col-span-2" key={i}>
            <div class="relative shadow-xl border border-white hover:-translate-y-1 duration-300 rounded-xl">
              <div class="bg-gray-800 flex rounded-xl p-6 lg:p-12 pt-0 lg:pt-0 relative object-cover">
                <img
                  src={portfolio.image}
                  alt={portfolio.title}
                  class="w-full h-[30vh] lg:h-[20vh] -mb-24 mt-12 rounded-xl"
                />
              </div>
              <div class="p-6 mt-12">
                <!-- <h4 class="text-2xl font-medium mb-4">{portfolio.title}</h4> -->
                <!-- Apply text truncation with ellipsis for up to 3 lines -->
                <!-- <p class="opacity-50 mb-0 overflow-hidden text-ellipsis line-clamp-3">{portfolio.description}</p> -->
                <div class="flex justify-between items-center px-7">
                    <!-- <a href={portfolio.href} target="_blank" class="px-5 py-2 rounded border border-blue-600 hover:text-white hover:bg-blue-600 duration-300 mt-6">
                        Demo
                      </a> -->
                      <a href={portfolio.git} target="_blank" class="px-5 py-2 rounded border border-purple-400 hover:text-white hover:bg-purple-400 duration-300 mt-6">
                        Code
                      </a> 
                </div>
              </div>
            </div>
          </div>
        {/each}
      </div>
    </div>
  </section>
  