<template>
  <div class="container mx-auto p-3 md:p-8">
    <div class="flex flex-col-reverse md:flex-row relative">
      <div class="w-full md:w-2/3">
        <!-- Search Bar -->
        <div class="mb-6 md:px-20">
          <div class="relative">
            <input 
              v-model="searchQuery"
              type="text" 
              placeholder="Search articles..."
              class="w-full bg-[#1e1e1f] border border-[#383838] rounded-xl text-white px-5 py-3 focus:outline-none focus:border-amber-200 transition-colors"
            >
            <svg class="absolute right-4 top-3.5 w-5 h-5 text-slate-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"></path>
            </svg>
          </div>
        </div>

        <div v-if="filteredArticles.length > 0" class="flex flex-col gap-4 md:px-20 fade-zoom-up">
          <article v-for="article in filteredArticles" :key="article.id">
            <a :href="article.url" target="_blank" class="flex w-full bg-[#1e1e1f] border-[#383838] rounded-xl text-left text-white p-5 md:py-7 md:px-8 cursor-pointer hover:bg-[#282828] items-center">
              <div class="w-full pr-4">
                <div class="text-xs mb-1 text-slate-400 flex items-center italic">
                  <div class="h-[1px] w-20 bg-amber-200 md:w-5 aos-init aos-animate mr-2"></div> {{ article.date }}
                </div>
                <h1 class="text-sm md:text-md text-amber-200 font-bold mb-2 paraf">{{ article.title }}</h1>
                <div class="text-sm hidden md:block paraf mb-3">{{ article.desc }}</div>
                <div class="text-xs text-amber-200 flex items-center hover:underline">
                  View Publication <svg class="ml-1 w-3 h-3" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"></path></svg>
                </div>
              </div>
              <div>
                <div class="w-20 h-20 md:w-28 flex items-center md:h-28">
                  <img :src="article.image" class="rounded-lg md:rounded-xl" alt="">
                </div>
              </div>
            </a>
          </article>
        </div>
        <div v-else class="text-center text-slate-400 md:px-20 py-10">
          No articles found for "{{ searchQuery }}"
          <button @click="searchQuery = ''; selectedTopic = 'All'" class="block mx-auto mt-4 text-amber-200 hover:underline">Clear all filters</button>
        </div>
      </div>
      <div class="w-full md:w-1/3 h-fit p-8 md:sticky md:top-24">
        <!-- Sidebar -->
        <div class="flex flex-col text-left">
          <div class="bg-clip-text bg-gradient-to-r from-slate-100 to-amber-300 text-transparent text-2xl font-bold">
            Publications
          </div>
          <div class="bg-clip-text bg-gradient-to-r from-slate-100 to-amber-300 text-transparent mt-2">
            Research papers and academic contributions in Data Science and Systems Development.
          </div>
          <div class="h-[1px] mt-7 mb-7 w-20 bg-amber-200 aos-init aos-animate mr-2"></div>
          <div class="hidden md:block">
            <div class="text-white text-md font-semibold text-amber-200">Topics</div>
            <div class="mt-3 flex flex-wrap gap-1">
              <span
                v-for="topic in topics"
                :key="topic"
                @click="selectedTopic = topic"
                :class="selectedTopic === topic ? 'bg-amber-200 text-black' : 'bg-[#1e1e1f] text-white hover:bg-white/20'"
                class="py-2 px-3 rounded-2xl text-xs cursor-pointer transition-colors"
              >{{ topic }}</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
  
<script>
export default {
  data() {
    return {
      searchQuery: '',
      selectedTopic: 'All',
      topics: ['All', 'Data Science', 'Machine Learning', 'Finance', 'Full-stack', 'Software Testing', 'Cybersecurity'],
      articles: [
        {
          id: 1,
          slug: 'perancangan-sistem-informasi-reservasi-badminton-agile',
          title: 'Perancangan Sistem Informasi Reservasi Lapangan Badminton Online Menggunakan Metode Agile (Studi Kasus: Daddies Arena Badminton)',
          date: 'Januari 2026',
          desc: 'Perkembangan teknologi informasi mendorong kebutuhan digitalisasi sistem layanan di berbagai sektor, termasuk penyewaan fasilitas olahraga. Penelitian ini bertujuan untuk merancang Sistem Informasi Reservasi Lapangan Badminton berbasis web menggunakan metode Agile guna meningkatkan efisiensi pengelolaan data, akurasi jadwal, serta kualitas layanan pelanggan. Hasil penelitian menunjukkan bahwa sistem mampu menyajikan informasi jadwal secara real-time dan meminimalisir tumpang tindih jadwal.',
          image: '/img/blog/badminton_reservasi.png',
          url: 'https://www.researchgate.net/publication/401281630_Perancangan_Sistem_Informasi_Reservasi_Lapangan_Badminton_Online_Menggunakan_Metode_Agile_Studi_Kasus_Daddies_Arena_Badminton',
          topic: 'Full-stack'
        },
        {
          id: 2,
          slug: 'analisis-big-data-harapan-hidup-global',
          title: 'ANALISIS BIG DATA TERHADAP DETERMINAN HARAPAN HIDUP GLOBAL: IMPLEMENTASI REGRESI LINEAR BERGANDA PADA 5.000+ DATASET WORLD DEVELOPMENT INDICATORS',
          date: 'Januari 2026',
          desc: 'Penelitian ini menganalisis pengaruh faktor makroekonomi (PDB per kapita dan tingkat pengangguran) terhadap angka harapan hidup global menggunakan pendekatan Big Data Analysis pada lebih dari 5.000 data Bank Dunia. Hasilnya menunjukkan bahwa PDB per kapita berpengaruh positif signifikan, sementara tingkat pengangguran berpengaruh negatif signifikan terhadap harapan hidup.',
          image: '/img/blog/harapan_hidup.png',
          url: 'https://www.researchgate.net/publication/401281532_ANALISIS_BIG_DATA_TERHADAP_DETERMINAN_HARAPAN_HIDUP_GLOBAL_IMPLEMENTASI_REGRESI_LINEAR_BERGANDA_PADA_5000_DATASET_WORLD_DEVELOPMENT_INDICATORS',
          topic: 'Data Science'
        },
        {
          id: 3,
          slug: 'pengujian-kualitas-perangkat-lunak-iso-29119',
          title: 'Pengujian Kualitas Perangkat Lunak Menggunakan Standar ISO/IEC/IEEE 29119 pada Sistem Informasi Reservasi Lapangan Badminton',
          date: 'Desember 2025',
          desc: 'Penelitian ini mengevaluasi kualitas fungsional Sistem Informasi Reservasi Lapangan Badminton menggunakan standar internasional ISO/IEC/IEEE 29119. Melalui penyusunan test plan dan test case, pengujian menunjukkan bahwa seluruh fungsi utama sistem seperti reservasi dan pengelolaan jadwal berjalan sesuai kebutuhan dan memenuhi standar kualitas yang ditetapkan.',
          image: '/img/blog/pengujian_kualitas.png',
          url: 'https://www.researchgate.net/publication/399136134_Pengujian_Kualitas_Perangkat_Lunak_Menggunakan_Standar_ISOIECIEEE_29119_pada_Sistem_Informasi_Reservasi_Lapangan_Badminton',
          topic: 'Software Testing'
        },
        {
          id: 4,
          slug: 'sistem-informasi-absensi-mahasiswa-web-qr-gps',
          title: 'Perancangan Sistem Informasi Absensi Mahasiswa Berbasis Web Dengan QR Code, Verifikasi Lokasi Gps, Dan Notifikasi Real-Time Menggunakan Metode Waterfall',
          date: 'Juli 2025',
          desc: 'Sistem ini dikembangkan untuk mengatasi manipulasi data pada absensi manual dengan memanfaatkan teknologi GPS dan QR Code. Dibangun dengan stack React.js, Express.js, dan MySQL, sistem ini memungkinkan verifikasi lokasi saat mahasiswa memindai kode QR. Fitur tambahan meliputi ekspor data ke PDF/CSV dan notifikasi real-time menggunakan Socket.IO.',
          image: '/img/blog/absensi_qr.png',
          url: 'https://scholar.google.com/citations?view_op=view_citation&hl=en&user=l0l33aYAAAAJ&citation_for_view=l0l33aYAAAAJ:u-x6o8ySG0sC',
          topic: 'Full-stack'
        },
        {
          id: 5,
          slug: 'sosialisasi-keamanan-digital-phishing-apk',
          title: 'Sosialisasi Keamanan Digital Untuk Mengatasi Phishing dan APK Berbahaya',
          date: 'Juni 2025',
          desc: 'Sosialisasi ini bertujuan meningkatkan kesadaran masyarakat terhadap ancaman phishing dan aplikasi (APK) berbahaya yang sering digunakan untuk mencuri data pribadi. Melalui seminar dan simulasi, peserta diajarkan cara mengenali situs palsu, pentingnya Autentikasi Dua Faktor (2FA), serta langkah aman dalam mengunduh aplikasi.',
          image: '/img/blog/keamanan_digital.png',
          url: 'https://scholar.google.com/citations?view_op=view_citation&hl=en&user=l0l33aYAAAAJ&citation_for_view=l0l33aYAAAAJ:u5HHmVD_uO8C',
          topic: 'Cybersecurity'
        }
      ]
    }
  },
  computed: {
    filteredArticles() {
      return this.articles.filter(article => {
        const matchesSearch = article.title.toLowerCase().includes(this.searchQuery.toLowerCase()) ||
                            article.desc.toLowerCase().includes(this.searchQuery.toLowerCase());
        const matchesTopic = this.selectedTopic === 'All' || article.topic === this.selectedTopic;
        return matchesSearch && matchesTopic;
      });
    }
  },
  components: {
  },
  mounted() {
    // Local data is already loaded in articles array
  },
  methods: {
    // Mock getArticles for compatibility if needed, but not used now
    getArticles() {
      return this.articles;
    }
  }
}
</script>

<style scoped>
.paraf {
  display: -webkit-box;
  -webkit-line-clamp: 3;
  line-clamp: 3;
  -webkit-box-orient: vertical;
  text-overflow: ellipsis;
  overflow: hidden;
}
@media (min-width: 768px) { 
  .paraf {
    display: -webkit-box;
  }
}
@keyframes fadeZoomUp {
  0% {
    opacity: 0;
    transform: scale(0.5);
  }
  100% {
    opacity: 1;
    transform: scale(1);
  }
}
.fade-zoom-up {
  animation: fadeZoomUp 1s ease-in-out;
  /* animation-delay: 1000ms; */
}
</style>