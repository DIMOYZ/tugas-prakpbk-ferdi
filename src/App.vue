<template>
 <nav class="navbar">
    <div class="brand-logo">Portofolio</div>
    <ul class="nav-links">
      <li><a href="#home" class="nav-item">Beranda</a></li>
      <li><a href="#about" class="nav-item">Tentang</a></li>
      <li><a href="#services" class="nav-item">Layanan</a></li>
      <li><a href="#contact" class="nav-item">Kontak</a></li>
    </ul>
    <div class="burger">
      <div class="line1"></div>
      <div class="line2"></div>
      <div class="line3"></div>
    </div>
  </nav>

  <div class="about-page">
    <section class="about-me">
      <h1>Ferdi Aldinata</h1>
      <img class="profile-pic" src="../src/assets/WhatsApp Image 2024-04-01 at 11.15.29 AM.jpeg" alt="Foto profil Anda" />
      <p>
        Nama saya adalah Ferdi Aldinata saya biasa dipanggil ferdi saya dilahirkan di padang japang pada tanggal 16 Desember 2003 saya merupakan anak pertama dari 4 bersaudara yang menuntut saya untuk bersikap dewasa kepada adik saya. Saya sekarang sebagai Mahasiswa di Universitas Islam Riau dengan jurusan Tenik Informatika , dan sekarang saya berada di semester 4.
      </p>
    </section>

    <div>
    <!-- Gambar pertama dengan penjelasan -->
    <div class="image-container">
      <img :src="image1" alt="Gambar Pertama">
      <p>{{ description1 }}</p>
    </div>

    <!-- Gambar kedua dengan penjelasan -->
    <div class="image-container">
      <img :src="image2" alt="Gambar Kedua">
      <p>{{ description2 }}</p>
    </div>
  </div>
    
 
  </div>

  <footer class="footer">
    <div class="container">
      <p>&copy; 2024 Your Name or Company Name. All Rights Reserved.</p>

      <ul class="social-links">
        <li v-for="link in socialLinks" :key="link.name">
          <a :href="link.url" target="_blank">
            <i :class="link.icon"></i>
          </a>
        </li>
      </ul>
    </div>
  </footer>

</template>

<script>
export default {
  data() {
    return {
      // Tautan ke gambar dan penjelasan
       // Jalur relatif ke gambar dan penjelasan
       image1: require('@/assets/1.jpg'),
      description1: 'Hobi saya adalah voly ball',
      image2: require('@/assets/2.jpg'),
      description2: 'Hobi saya adalah Berenang'
    }
  }
}

</script>

<style>
.social-media-page {
  text-align: center;
  margin-top: 2rem;
}

.social-icons {
  margin-top: 1rem;
}

.social-icon {
  font-size: 2rem;
  margin: 0 0.5rem;
  color: #b90505;
  transition: color 0.3s ease;
}

.social-icon:hover {
  color: #be500b;
}

/* Tambahkan kelas FontAwesome di sini atau impor melalui CDN */
.image-container {
  margin: 20px 0;
  text-align: center; /* Teks penjelasan akan berada di tengah di bawah gambar */
  transition: transform 0.3s ease; /* Transisi halus saat di-hover */
}

.image-container:hover {
  transform: scale(1.05); /* Membesar sedikit saat di-hover */
}

.image-container img {
  max-width: 20%; /* Mengatur lebar gambar menjadi setengah dari lebar maksimum */
  height: auto; /* Menjaga rasio aspek gambar */
  margin-bottom: 10px; /* Memberi jarak antara gambar dan teks penjelasan */
  border-radius: 10px; /* Memberikan sudut yang melengkung pada gambar */
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Menambahkan bayangan pada gambar */
  transition: all 0.3s ease; /* Transisi halus untuk bayangan dan transformasi */
  display: block; /* Membuat gambar menjadi blok sehingga margin otomatis berfungsi */
  margin-left: auto; /* Margin otomatis untuk menyelaraskan gambar ke tengah */
  margin-right: auto; /* Margin otomatis untuk menyelaraskan gambar ke tengah */
}

.image-container img:hover {
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2); /* Bayangan yang lebih besar saat di-hover */
}

.image-container p {
  font-size: 16px; /* Ukuran font untuk teks penjelasan */
  color: #333; /* Warna font untuk teks penjelasan */
  background-color: #f8f8f8; /* Latar belakang untuk teks penjelasan */
  padding: 10px; /* Padding di sekitar teks */
  border-radius: 5px; /* Sudut yang melengkung pada latar belakang teks */
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1); /* Bayangan pada latar belakang teks */
}

/* Animasi Gradien yang Berubah-ubah */
@keyframes gradientBackground {
  0% { background-color: #6a3093; }
  50% { background-color: #a044ff; }
  100% { background-color: #6a3093; }
}
.image-container {
  margin-bottom: 20px;
}
img {
  width: 100%;
  height: auto;
}
.footer {
  animation: gradientBackground 5s ease infinite;
  background-color: #343a40; /* Warna latar awal */
  color: #fff;
  padding: 1rem 2rem;
  text-align: center;
}

/* Tambahkan efek hover pada ikon media sosial */
.social-links i:hover {
  transform: scale(1.1);
  color: #a044ff; /* Ubah warna saat hover */
}


.about-page {
  padding: 2rem;
  background-color: #ffff00; /* Warna kuning */
}


/* Sisanya dari kode CSS Anda tetap sama */

.about-me {
  text-align: center;
}

.profile-pic {
  width: 150px;
  border-radius: 50%;
}

.my-work {
  display: flex;
  flex-wrap: wrap;
}

.work-item {
  margin: 1rem;
  width: 300px;
  padding: 1rem;
  border: 1px solid #ddd;
  border-radius: 10px;
}

.work-image {
  width: 100%;
}


@keyframes gradientBG {
  0% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
  100% {
    background-position: 0% 50%;
  }
}

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem;
  background: linear-gradient(-45deg, #3498db, #ffffff, #f1c40f);
  background-size: 400% 400%;
  animation: gradientBG 15s ease infinite;
}

/* Sisanya sama seperti kode CSS Anda sebelumnya */

.brand-logo {
  color: #fff;
  font-size: 1.5rem;
}

.nav-links {
  display: flex;
  list-style: none;
}

.nav-item {
  color: #fff;
  text-decoration: none;
  padding: 1rem;
  transition: background-color 0.3s;
}

.nav-item:hover {
  background-color: #555;
}

.burger {
  display: none;
  cursor: pointer;
}

.burger div {
  width: 25px;
  height: 3px;
  background-color: #fff;
  margin: 5px;
  transition: all 0.3s ease;
}

/* Responsif */
@media screen and (max-width: 768px) {
  .nav-links {
    position: absolute;
    right: 0;
    height: 92vh;
    top: 8vh;
    background-color: #333;
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 50%;
    transform: translateX(100%);
    transition: transform 0.5s ease-in;
  }

  .nav-links.nav-active {
    transform: translateX(0%);
  }

  .burger {
    display: block;
  }

  .burger.toggle .line1 {
    transform: rotate(-45deg) translate(-5px, 6px);
  }

  .burger.toggle .line2 {
    opacity: 0;
  }

  .burger.toggle .line3 {
    transform: rotate(45deg) translate(-5px, -6px);
  }
}
</style>
