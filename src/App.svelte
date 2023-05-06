<script>
  import AOS from "aos";
  import { onMount } from 'svelte';
  import "aos/dist/aos.css";
  let name = "</ARVIND SRIVASTAV>";
  let about = "</ABOUT ME>";
  let education = "</EDUCATION>";
  let work = "</WORK AND PROJECTS>";
  let Matric = "</matric>";

  AOS.init();
  let isMobileMenuOpen = false;

  function toggleMobileMenu() {
    isMobileMenuOpen = !isMobileMenuOpen;
  }

  
  let screenSize;

  const updateScreenSize = () => {
    screenSize = window.innerWidth < 768 ? 'mobile' : 'desktop';
  }

  onMount(() => {
    updateScreenSize();
    window.addEventListener('resize', updateScreenSize);
  });
</script>

<!-- Navbar -->
<nav class="bg-purple-500 sm:self-center justify-content-center h-20">
  <div class="container mx-auto flex items-center justify-between ">
    <div>
      <img
        class="w-20 h-20 rounded-full"
        src="https://avatars.githubusercontent.com/u/94129388?v=4"
       alt="githubimg">
    </div>
    <h5 class="text-white text-4xl font-bold p-3 {screenSize === 'mobile' ? 'ml-4' : '-ml-96'}">
      <hr />
      {name}
      <hr />
    </h5>
    <div class="sm:hidden">
      <button
        type="button"
        class="text-white hover:text-gray-300 focus:outline-none"
        on:click={toggleMobileMenu}
      >
        <svg
          class="h-6 w-6 fill-current"
          viewBox="0 0 24 24"
          xmlns="http://www.w3.org/2000/svg"
        >
          <title>Mobile menu</title>
          <path
            class={isMobileMenuOpen ? 'hidden' : 'block'}
            d="M4 6h16M4 12h16M4 18h16"
            stroke="#fff"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
          />
          <path
            class={isMobileMenuOpen ? 'block' : 'hidden'}
            d="M6 18L18 6M6 6l12 12"
            stroke="#fff"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
          />
        </svg>
      </button>
    </div>
    <div class="hidden sm:block">
      <ul class="text-white font-extrabold text-3xl border-t sm:border-none">
        <li class="inline-block mr-4  scale-100 hover:scale-125 ease-in duration-100">
          <a href="/">ABOUT</a>
        </li>
        <li class="inline-block mr-4  scale-100 hover:scale-125 ease-in duration-100">
          <a href="/">EDUCATION</a>
        </li>
        <li class="inline-block mr-4  scale-100 hover:scale-125 ease-in duration-100">
          <a href="/">WORK</a>
        </li>
        <li class="inline-block mr-4  scale-100 hover:scale-125 ease-in duration-100">
          <a href="/">SKILLS</a>
        </li>
        <li class="inline-block mr-4  scale-100 hover:scale-125 ease-in duration-100">
          <a href="/">CONTACT</a>
        </li>
        <li class="inline-block  scale-100 hover:scale-125 ease-in duration-100">
          <a href="/">RESUME</a>
        </li>
      </ul>
    </div>
  </div>
  <div class={`sm:hidden bg-purple-500 px-4 pt-2 pb-3 ${ isMobileMenuOpen ? 'block' : 'hidden'}`}>
  {#if isMobileMenuOpen}

    <ul class="text-white font-extrabold text-3xl">
      <li class="block mb-2">
        <a href="/" on:click={toggleMobileMenu}>ABOUT</a>
      </li>
      <li class="block mb-2">
        <a href="/" on:click={toggleMobileMenu}>EDUCATION</a>
      </li>
      <li class="block mb-2">
        <a href="/" on:click={toggleMobileMenu}>WORK</a>
      </li>
      <li class="block mb-2">
        <a href="/" on:click={toggleMobileMenu}>SKILLS</a>
      </li>
      <li class="block mb-2">
        <a href="/" on:click={toggleMobileMenu}>CONTACT</a>
      </li>
      <li class="block mb-2">
        <a href="/" on:click={toggleMobileMenu}>RESUME</a>
      </li>
    </ul>
{/if}
  </div>
</nav>
<section>
  <div data-aos="zoom-in" class="bg-black">
    <div class="container mx-auto text-items:center">
      <h2
        class="text-white text-4xl font-bold p-3 text-align:center "
        style="text-align: center"
       >
        {about}
      </h2>
    </div>

    <hr />
    <div class="container mx-auto px-4 " id="text">

      <h4 class="text-white text-xl font-serif p-3 leading-8 py-4">
        Yo, what's good peeps! Thank you for your visit to my website .My name is
        Arvind Srivastav and I'm reppin' Sultanpur, but right now I'm chillin'
        in Lucknow. I'm currently pursuing a B.Tech/B.E. in Computers from the
        University of Lucknow, which I'll be completing in Jul-2024. My GPA is a
        solid 8.4 out of 10, just sayin'. My degree in Computers has equipped me
        with all the dope skills I need to thrive in the industry. Lately, I've
        been tryna cultivate a reading habit  . I also love connecting with my OGs and
        cousins who are crushing it at top companies. Their grind and hustle
        motivate me to push harder. When it comes to my project experience, I've
        put in 3 months of work on some super intriguing topics like Education
        Institute Website and Telegram Weather Bot. In terms of my academic
        record, I killed it in my XIIth CBSE Senior Secondary exam with a score
        of 91.4% in English medium. And in Xth CBSE Board, I slayed with a solid
        93.4%. School and college have played a massive role in shaping me into
        a well-rounded individual. I've been given opportunities to contribute
        to various projects and activities, and I've excelled in them. My
        institutions have taught me that passion is key to success. I'm
        constantly tryna level up my skills so that I can bring more value to a
        dope company like yours. By the way, I'm well-versed in Python, Django,
        Django Rest API, Web Development, Linux, Web Scraping, Postman API,
        Github and Flask Web Framework. One more thing, I'm a quick learner and
        believe that learning from my mistakes is key to success in life and
        career.
      </h4>
    </div>
  </div>
</section>

<section>
  <div data-aos="zoom-in" class="bg-purple-500 opacity-75">
    <div class="container mx-auto text-items:center">
      <h2
        class="text-white text-4xl font-bold p-3 text-align:center"
        style="text-align: center"
      >
        {education}
      </h2>
    </div>
    <hr />
    <div
      class="p-10 grid grid-cols-1 sm:grid-cols-1 md:grid-cols-3 lg:grid-cols-3 xl:grid-cols-3 gap-5"
    >
      <div
        class=" overflow-hidden hover:shadow-lg  scale-100 hover:scale-105 ease-in duration-300
       "
        style="
      border-radius: 43px;
      background: linear-gradient(225deg, #ab22ff, #901dd8);
      box-shadow:  -13px 13px 24px #921dda,
                   13px -13px 24px #ae23ff;"
      >
        <div class="px-6 py-4 relative">
          <div class="font-bold text-3xl mb-2 relative">{Matric}</div>
          <h2 class="text-white text-2xl font-serif p-3">
            Completed class 10th scoring 9.8CGPA from Stella Maris Convent School,Sultanpur
          </h2>
        </div>
        <div class="px-6 pt-4 pb-2">
          <span
            class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-2"
            >#photography</span
          >
          <span
            class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-2"
            >#travel</span
          >
          <span
            class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-2"
            >#winter</span
          >
        </div>
      </div>
      <div
        class="rounded overflow-hidden shadow-2xl hover:shadow-white scale-100 hover:scale-105 ease-in duration-300"
        style="
      border-radius: 43px;
      background: linear-gradient(225deg, #ab22ff, #901dd8);
      box-shadow:  -13px 13px 24px #921dda,
                   13px -13px 24px #ae23ff;"
      >
        <div class="px-6 py-4">
          <div class="font-bold text-xl mb-2">River</div>
          <h2 class="text-white text-2xl font-serif p-3">
            Completed class 12th scoring 91.4% from Stella Maris Convent School,Sultanpur

          </h2>
        </div>
        <div class="px-6 pt-4 pb-2">
          <span
            class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-2"
            >#photography</span
          >
          <span
            class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-2"
            >#travel</span
          >
          <span
            class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-2"
            >#summer</span
          >
        </div>
      </div>

      <div
        class="rounded overflow-hidden shadow-2xl hover:shadow-white hover:shadow-2xl"
        style="
      border-radius: 43px;
      background: linear-gradient(225deg, #ab22ff, #901dd8);
      box-shadow:  -13px 13px 24px #921dda,
                   13px -13px 24px #ae23ff;"
      >
        <div class="px-6 py-4">
          <div class="font-bold text-xl mb-2">Forest</div>
          <h2 class="text-white text-2xl font-serif p-3">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit.
            Voluptatibus quia, Nonea! Maiores et perferendis eaque,
            exercitationem praesentium nihil.
          </h2>
        </div>
        <div class="px-6 pt-4 pb-2">
          <span
            class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-2"
            >#photography</span
          >
          <span
            class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-2"
            >#travel</span
          >
          <span
            class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-2"
            >#fall</span
          >
        </div>
      </div>
    </div>
  </div>
</section>

<section>
  <div data-aos="zoom-in" class="bg-white opacity-75" id="id">
    <div class="container mx-auto text-items:center">
      <h2
        class="text-black text-4xl font-bold p-3 "
        style="text-align: center"
      >
        {work}
      </h2>
    </div>
    <hr />

  <div class="container mx-auto py-12 w-full " >
    <div class=" grid grid-cols-1 sm:grid-cols-1 md:grid-cols-3 lg:grid-cols-3 xl:grid-cols-3 " style="gap: 11.25rem;" >
      <div class=" max-w-sm rounded overflow-hidden  scale-100 shadow-white hover:scale-125 ease-in duration-500">
        <img class="w-full" src="assets/project1.png" alt="project1">
        <div class="px-6 py-4">
          <div class="font-bold text-xl mb-2">project1</div>
          <p class="text-white text-base ">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatibus quia, nulla! Maiores et perferendis eaque, exercitationem praesentium nihil.
          </p>
        </div>
        <div class="px-6 pt-4 pb-2">
          <span class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-2">#photography</span>
          <span class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-2">#travel</span>
          <span class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-2">#winter</span>
        </div>
      </div>
      <div class="max-w-sm rounded overflow-hidden shadow-lg scale-100 hover:scale-125 ease-in duration-500">
        <img class="w-full" src="assets/project1.png" alt="Sunset in the mountains">
        <div class="px-6 py-4">
          <div class="font-bold text-xl mb-2">The Coldest Sunset</div>
          <p class="text-white text-base">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatibus quia, nulla! Maiores et perferendis eaque, exercitationem praesentium nihil.
          </p>
        </div>
        <div class="px-6 pt-4 pb-2">
          <span class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-2">#photography</span>
          <span class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-2">#travel</span>
          <span class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-2">#winter</span>
        </div>
      </div>
      <div class="max-w-sm rounded overflow-hidden shadow-lg scale-100 hover:scale-125 ease-in duration-500">
        <img class="w-full" src="assets/project1.png" alt="Sunset in the mountains">
        <div class="px-6 py-4">
          <div class="font-bold text-xl mb-2">The Coldest Sunset</div>
          <p class="text-white text-base">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatibus quia, nulla! Maiores et perferendis eaque, exercitationem praesentium nihil.
          </p>
        </div>
        <div class="px-6 pt-4 pb-2">
          <span class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-2">#photography</span>
          <span class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-2">#travel</span>
          <span class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-2">#winter</span>
        </div>
      </div>
      
  </div>


</div>

</section>