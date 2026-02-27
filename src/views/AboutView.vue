<script>
export default {
  data() {
    return {
      activeTab: 1,
      tech: [
        {
          id: 1,
          name: 'Python',
          imageUrl: 'https://cdn.iconscout.com/icon/free/png-256/free-python-3521655-2945099.png',
          status: 'Advanced'
        },
        {
          id: 2,
          name: 'SQL',
          imageUrl: 'https://cdn-icons-png.flaticon.com/512/2772/2772128.png',
          status: 'Advanced'
        },
        {
          id: 3,
          name: 'Javascript',
          imageUrl: 'https://cdn.icon-icons.com/icons2/2415/PNG/512/javascript_original_logo_icon_146455.png',
          status: 'Advanced'
        },
        {
          id: 4,
          name: 'TypeScript',
          imageUrl: 'https://cdn-icons-png.flaticon.com/512/5968/5968381.png',
          status: 'Intermediate'
        },
        {
          id: 5,
          name: 'ReactJS',
          imageUrl: 'https://cdn4.iconfinder.com/data/icons/logos-3/600/React.js_logo-512.png',
          status: 'Intermediate'
        },
        {
          id: 6,
          name: 'NextJS',
          imageUrl: 'https://img.icons8.com/nolan/64/nextjs.png',
          status: 'Intermediate'
        },
        {
          id: 7,
          name: 'NodeJS',
          imageUrl: 'https://cdn.iconscout.com/icon/free/png-256/free-node-js-1174925.png',
          status: 'Intermediate'
        },
        {
          id: 8,
          name: 'ExpressJS',
          imageUrl: 'https://img.icons8.com/ios/50/ffffff/express-js.png',
          status: 'Intermediate'
        },
        {
          id: 9,
          name: 'FastAPI',
          imageUrl: 'https://fastapi.tiangolo.com/img/favicon.png',
          status: 'Intermediate'
        },
        {
          id: 10,
          name: 'Machine Learning',
          imageUrl: 'https://cdn-icons-png.flaticon.com/512/2103/2103633.png',
          status: 'Advanced'
        },
        {
          id: 11,
          name: 'MongoDB',
          imageUrl: 'https://img.icons8.com/color/48/000000/mongodb.png',
          status: 'Intermediate'
        },
        {
          id: 12,
          name: 'PostgreSQL',
          imageUrl: 'https://img.icons8.com/color/48/000000/postgreesql.png',
          status: 'Advanced'
        },
        {
          id: 13,
          name: 'MySQL',
          imageUrl: 'https://img.icons8.com/color/48/000000/mysql-logo.png',
          status: 'Advanced'
        },
        {
          id: 14,
          name: 'Tailwind CSS',
          imageUrl: 'https://upload.wikimedia.org/wikipedia/commons/d/d5/Tailwind_CSS_Logo.svg',
          status: 'Advanced'
        },
        {
          id: 15,
          name: 'Bootstrap',
          imageUrl: 'https://getbootstrap.com/docs/5.2/assets/brand/bootstrap-logo-shadow.png',
          status: 'Intermediate'
        },
        {
          id: 16,
          name: 'React Native',
          imageUrl: 'https://cdn.worldvectorlogo.com/logos/react-native-1.svg',
          status: 'Beginner'
        },
        {
          id: 17,
          name: 'Docker',
          imageUrl: 'https://img.icons8.com/color/48/000000/docker.png',
          status: 'Intermediate'
        },
        {
          id: 18,
          name: 'PHP',
          imageUrl: 'https://img.icons8.com/officel/40/000000/php-logo.png',
          status: 'Intermediate'
        }
      ],
      tools: [
        {
          id: 1,
          name: 'Git',
          imageUrl: 'https://git-scm.com/images/logos/downloads/Git-Icon-1788C.png',
          status: 'Version Control'
        },
        {
          id: 2,
          name: 'GitHub',
          imageUrl: 'https://img.icons8.com/ios-filled/50/ffffff/github.png',
          status: 'Git Hosting'
        },
        {
          id: 3,
          name: 'Figma',
          imageUrl: 'https://cdn-icons-png.flaticon.com/512/5968/5968705.png',
          status: 'Design Tool'
        },
        {
          id: 4,
          name: 'NPM',
          imageUrl: 'https://cdn.iconscout.com/icon/free/png-256/free-npm-3-1175132.png',
          status: 'Package Manager'
        },
        {
          id: 5,
          name: 'Tableau',
          imageUrl: 'https://img.icons8.com/color/48/000000/tableau-software.png',
          status: 'Data Visualization'
        },
        {
          id: 6,
          name: 'Power BI',
          imageUrl: 'https://img.icons8.com/color/48/000000/power-bi.png',
          status: 'Business Intelligence'
        },
        {
          id: 7,
          name: 'Airflow',
          imageUrl: 'https://upload.wikimedia.org/wikipedia/commons/d/de/AirflowLogo.png',
          status: 'Orchestration'
        },
        {
          id: 8,
          name: 'AWS',
          imageUrl: 'https://img.icons8.com/color/48/000000/amazon-web-services.png',
          status: 'Cloud'
        },
        {
          id: 9,
          name: 'Terraform',
          imageUrl: 'https://img.icons8.com/color/48/000000/terraform.png',
          status: 'Infrastructure as Code'
        }
      ]
    };
  }
}
</script>
<template>
  <div
    class="bg-[#1e1e1f] px-5 py-5 md:px-12 md:py-10 text-left border border-[#383838] rounded-3xl text-amber-50 mx-3 mb-5">
    <article data-page="about">

      <header>
        <div class="text-2xl font-bold text-white mb-5 fadein-bot title-section flex items-center">
          About Me &nbsp;
          <div class="h-[1px] w-32 bg-amber-200 md:w-96 aos-init aos-animate" data-aos="zoom-in-left"
            data-aos-duration="600"></div>
        </div>
      </header>

      <section
        class="text-sm md:text-lg text-justify flex flex-col gap-4 md:flex-row md:gap-8 md:justify-left md:items-center">
        <div class="flex justify-center">
          <img class="w-9/12 rounded-full mb-3 fadein-up"
            src="/img/avatar.jpg" alt="Foto">
        </div>
        <div class="md:w-7/12">
          <p class="mb-3 md:mb-7 fadein-left fadeins-1 text-justify">
            &nbsp; &nbsp; &nbsp; I am <b>Mohammad Satria Arya Buminata</b>, a high-achieving Information Systems professional at Universitas Pamulang (GPA 3.90/4.00). I specialize in bridging the gap between <b>Advanced Data Analytics</b> and <b>Full-stack Systems Architecture</b>. My mission is to translate complex datasets into scalable, intelligent solutions that drive strategic value.
          </p>
          <p class="mb-3 fadein-left fadeins-2 text-justify">
            &nbsp; &nbsp; &nbsp; As a multi-certified professional (AWS, Associate Data Scientist, Financial Analyst), I bring a unique hybrid expertise in building robust web applications and engineering precise data pipelines. My toolkit spans from machine learning models with Python to high-performance interfaces with React and Next.js, always focused on delivering efficiency and operational excellence.
          </p>
          <div class="mt-5 flex flex-col gap-2 text-sm text-amber-200 fadein-left fadeins-3">
            <div class="flex items-center gap-2">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
              </svg>
              <span>Tangerang Selatan, Banten</span>
            </div>
            <div class="flex items-center gap-2">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
              </svg>
              <a href="mailto:aryabuminata21@gmail.com" class="hover:underline">aryabuminata21@gmail.com</a>
            </div>
            <div class="flex items-center gap-2">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z" />
              </svg>
              <span>+62 877-6587-6684</span>
            </div>
          </div>
          <div class="mt-6 fadein-left fadeins-3 flex flex-wrap gap-4">
             <a href="https://linkedin.com/in/mohammad-satria-arya-" target="_blank" class="flex items-center gap-2 w-fit px-4 py-2 rounded-lg bg-amber-200 text-black font-semibold hover:bg-amber-300 transition-colors">
               <svg class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24"><path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.761 0 5-2.239 5-5v-14c0-2.761-2.239-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/></svg>
               LinkedIn
             </a>
             <a href="https://drive.google.com/file/d/1cNpLT4Tsfds_lktAxUTNElbnJc9ckGhc/view?usp=drive_link" target="_blank" class="flex items-center gap-2 w-fit px-4 py-2 rounded-lg border border-amber-200 text-amber-200 font-semibold hover:bg-amber-200 hover:text-black transition-all">
               <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                 <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 10v6m0 0l-3-3m3 3l3-3m2 8H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z" />
               </svg>
               Download CV
             </a>
          </div>
        </div>

      </section>

    </article>
  </div>

  <div class="px-5 py-5 md:px-12 md:py-10 text-left text-amber-50 mx-3">
    <article data-page="about">
      <header>
        <div class="text-2xl font-bold text-white mb-5 fadein-bot title-section flex items-center">
          <div class="h-[1px] w-10 bg-amber-200 md:w-20 aos-init aos-animate" data-aos="zoom-in-left"
            data-aos-duration="600"></div>
          &nbsp; Skills
        </div>
      </header>
      <section>
        <div>
          <ul class="flex flex-wrap text-sm font-medium text-center text-gray-500 dark:text-gray-400 mb-5">
            <li class="mr-2">
              <button class="inline-block px-4 py-3 rounded-lg hover:text-white"
                :class="{ 'text-amber-200 bg-amber-200 bg-opacity-10': activeTab === 1 }" @click="activeTab = 1">Tech Stack</button>
            </li>
            <li class="mr-2">
              <button class="inline-block px-4 py-3 rounded-lg hover:text-white"
                :class="{ 'text-amber-200 bg-amber-200 bg-opacity-10': activeTab === 2 }" @click="activeTab = 2">Tools</button>
            </li>
          </ul>
        </div>
        <div v-show="activeTab === 1">
          <div class="grid grid-cols-2 gap-4 pb-32 md:grid-cols-3 md:gap-8 xl:grid-cols-4 xl:gap-10 2xl:gap-12">
            <div v-for="item in tech" :key="item.id">
              <div
                class="item-tech flex cursor-pointer items-center gap-2 rounded border border-amber-200 px-2 py-2 hover:bg-amber-200 hover:bg-opacity-10 md:gap-3 lg:px-3">
                <div class="flex h-12 w-12 items-center justify-center p-0 lg:h-16 lg:w-16 lg:p-2 zoom-in">
                  <img alt="HTML" loading="lazy" width="32" height="32" decoding="async" data-nimg="1"
                    class="img-tech drop-shadow-xl transition-all duration-300 h-[65%] w-[65%] lg:h-[85%] lg:w-[85%]  "
                    :src="item.imageUrl" style="color: transparent;">
                </div>
                <div class="flex items-center text-sm md:text-base lg:text-lg">
                  <div class="tech font-medium text-secondary transition-all duration-300 translate-y-0 ">{{ item.name }}
                  </div>
                  <div
                    class="status-tech opacity-0 absolute mt-5 text-[10px] text-amber-200 transition-all duration-300 md:text-xs lg:text-sm">
                    {{ item.status }}</div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div v-show="activeTab === 2">
          <div class="grid grid-cols-2 gap-4 pb-32 md:grid-cols-3 md:gap-8 xl:grid-cols-4 xl:gap-10 2xl:gap-12">
            <div v-for="item in tools" :key="item.id">
              <div
                class="item-tech flex cursor-pointer items-center gap-2 rounded border border-amber-200 px-2 py-2 hover:bg-amber-200 hover:bg-opacity-10 md:gap-3 lg:px-3">
                <div class="flex h-12 w-12 items-center justify-center p-0 lg:h-16 lg:w-16 lg:p-2 zoom-in">
                  <img alt="HTML" loading="lazy" width="32" height="32" decoding="async" data-nimg="1"
                    class="img-tech drop-shadow-xl transition-all duration-300 h-[65%] w-[65%] lg:h-[85%] lg:w-[85%]  "
                    :src="item.imageUrl" style="color: transparent;">
                </div>
                <div class="flex items-center text-sm md:text-base lg:text-lg">
                  <div class="tech font-medium text-secondary transition-all duration-300 translate-y-0 ">{{ item.name }}
                  </div>
                  <div
                    class="status-tech opacity-0 absolute mt-5 text-[10px] text-amber-200 transition-all duration-300 md:text-xs lg:text-sm">
                    {{ item.status }}</div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
    </article>
  </div>
</template>

<style>
.fadein-left {
  opacity: 0;
  animation: fadeInLeft 0.5s ease-out forwards;
}

@keyframes fadeInLeft {
  0% {
    opacity: 0;
    transform: translateX(100%);
  }

  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

.fadeins-1 {
  animation-delay: 500ms;
}

.fadeins-2 {
  animation-delay: 800ms;
}

.fadeins-3 {
  animation-delay: 1100ms;
}

.img-tech,
.tech {
  transition: transform 0.3s ease;
}

.item-tech:hover .img-tech {
  transform: scale(1.3);
}

.item-tech:hover .tech {
  transform: translateY(-12px);
}

.item-tech:hover .status-tech {
  opacity: 1;
}
</style>
