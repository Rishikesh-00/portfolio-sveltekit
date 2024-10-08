<script>
    import Resume from "../assets/Rishikesh_resume.pdf";
  
    const links = [
      {
        id: 1,
        child: "LinkedIn",
        icon: "bx bxl-linkedin",
        href: "https://linkedin.com",
        style: "rounded-tr-md",
      },
      {
        id: 2,
        child: "Github",
        icon: "bx bxl-github",
        href: "https://github.com/Rishikesh-00",
      },
      {
        id: 3,
        child: "Mail",
        icon: "bx bx-envelope",
        href: "mailto:keshrishi1789@gmail.com",
      },
      {
        id: 4,
        child: "Resume",
        icon: "bx bxs-user-detail",
        href: Resume,
        style: "rounded-br-md",
        download: true,
      },
    ];
  </script>
  
  <div class="hidden lg:flex flex-col top-[35%] left-0 fixed">
    <ul>
      {#each links as { id, child, icon, href, style, download }}
        <li
          key={id}
          class={"flex justify-between items-center w-40 h-14 px-4 bg-gray-500 bg-opacity-100 ml-[-100px] hover:ml-[-10px] hover:rounded-md duration-300 " + (style || "")}
        >
          <a
            href={href}
            class="flex justify-between items-center w-full text-white"
            download={download}
            target="_blank"
            rel="noopener noreferrer"
          >
            {child} <i class={icon} style="font-size: 30px;"></i>
          </a>
        </li>
      {/each}
    </ul>
  </div>
  