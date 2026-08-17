<script setup>
import { computed, ref } from 'vue'

const nama = ref('')
const noTelp = ref('')
const kebutuhan = ref('')

const mailtoHref = computed(() => {
  const subject = encodeURIComponent(
    `Permintaan dari ${nama.value || 'Customer'}${noTelp.value ? ` (${noTelp.value})` : ''}`,
  )

  const body = encodeURIComponent(
    [
      `Nama: ${nama.value || '-'}`,
      `No Telp: ${noTelp.value || '-'}`,
      'Deskripsi Kebutuhan:',
      kebutuhan.value || '-',
    ].join('\n'),
  )

  return `mailto:trimagnasinergimakmur@gmail.com?subject=${subject}&body=${body}`
})
</script>

<template>
  <main>
    <div id="beranda" class="banner-container">
      <div class="banner-image-background">
        <img src="https://picsum.photos/1000" alt="banner" />
      </div>
      <div class="banner-content-container">
        <div class="banner-content-layout">
          <div class="banner-content-layout-row"></div>
          <div class="banner-content-layout-row">
            <div class="banner-content-header">TRIMAGNA SINERGI MAKMUR</div>
            <div class="banner-content-header">
              <h1>Penyedia Produk Besi Baja untuk Kebutuhan Proyek</h1>
            </div>
          </div>
          <div class="banner-content-layout-row">
            <a href="mailto:trimagnasinergimakmur@gmail.com">
              <button><i class="bi bi-envelope"></i> Hubungi Kami</button>
            </a>
          </div>
        </div>
      </div>
    </div>

    <div class="unggulan-container">
      <div class="unggulan-layout">
        <div>
          <h1>TRIMAGNA SINERGI MAKMUR</h1>
          <br />
          <p>
            Trimagna Sinergi Makmur adalah perusahaan yang bergerak pada distribusi besi dan baja,
            dioperasikan oleh tenaga kerja profesional. Kami memiliki variasi jenis produk dan grade
            yang beragam sehingga kami memastikan kebutuhan proyek terpenuhi. Bekerja sama dengan
            beberapa merk besar. Semuanya telah memenuhi Standar Nasional Indonesia (SNI).
          </p>
        </div>
        <div class="unggulan-image-container">
          <img src="https://picsum.photos/1020" alt="deskripsi-perusahaan" />
        </div>
      </div>
    </div>

    <div id="produk-tsm" class="items">
      <div class="item-container">
        <div class="item-background-image-container">
          <div class="item-background-image">
            <img src="@/assets/projecta.jpeg" alt="Item Image" />
          </div>
          <div class="item-title">Project</div>
        </div>
      </div>
      <div class="item-container">
        <div class="item-background-image-container">
          <div class="item-background-image">
            <img src="@/assets/projectb.jpeg" alt="Item Image" />
          </div>
          <div class="item-title">Project</div>
        </div>
      </div>
      <div class="item-container">
        <div class="item-background-image-container">
          <div class="item-background-image">
            <img src="@/assets/projectc.jpeg" alt="Item Image" />
          </div>
          <div class="item-title">Project</div>
        </div>
      </div>
    </div>

    <div class="maps">
      <iframe
        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3965.5746457518453!2d107.16725199999999!3d-6.3194669999999995!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2e699b0de98f0dad%3A0x2e2356c1967fc0ed!2sJl.%20Anoa%202%20No.112%2C%20RT.2%2FRW.8%2C%20Jayamukti%2C%20Kec.%20Cikarang%20Pusat%2C%20Kabupaten%20Bekasi%2C%20Jawa%20Barat%2017530!5e0!3m2!1sen!2sid!4v1786932549238!5m2!1sen!2sid"
        width="400"
        height="300"
        style="border: 0"
        allowfullscreen=""
        loading="lazy"
        referrerpolicy="strict-origin-when-cross-origin"
      ></iframe>
    </div>

    <section id="kontak" class="contact-form-section">
      <div class="contact-form-card">
        <div class="contact-form-header">
          <h2>Kirim Kebutuhan Anda</h2>
          <p>
            Isi detail kebutuhan proyek Anda, lalu klik tombol di bawah untuk mengirim via email.
          </p>
        </div>

        <div class="contact-form">
          <label class="contact-field">
            <span>Nama</span>
            <input v-model="nama" type="text" placeholder="Masukkan nama Anda" />
          </label>

          <label class="contact-field">
            <span>No Telp</span>
            <input v-model="noTelp" type="tel" placeholder="Masukkan nomor telepon" />
          </label>

          <label class="contact-field">
            <span>Deskripsi Kebutuhan</span>
            <textarea
              v-model="kebutuhan"
              rows="5"
              placeholder="Jelaskan kebutuhan proyek atau produk yang Anda cari"
            ></textarea>
          </label>
        </div>

        <a :href="mailtoHref" class="mailto-button">
          <i class="bi bi-envelope"></i>
          Kirim via Email
        </a>
      </div>
    </section>
  </main>
</template>

<style scoped>
.banner-container {
  width: 100%;
  height: 50vh;
  background-color: red;
  position: relative;
}

.banner-image-background {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: red;
}

.banner-image-background img {
  width: 100%;
  height: 100%;
  filter: brightness(50%);
  object-fit: cover;
}

.banner-content-container {
  position: relative;
  width: 100%;
  height: 100%;
}

.banner-content-header {
  color: white;
}

.banner-content-layout {
  height: 100%;
  display: grid;
  grid-template-rows: repeat(3, 1fr);
}

.banner-content-layout-row {
  padding: 1em;
}

.banner-content-layout-row button {
  background-color: red;
  border: none;
  border-radius: 8px;
  padding: 0.75em 1.25em;

  color: white;

  display: flex;
  align-items: center;
  gap: 0.5em;

  font-size: 1rem;
  font-weight: bold;
  cursor: pointer;
}

.banner-content-layout-row button i {
  font-size: 1.25rem;
}

.unggulan-container {
  position: relative;
  width: 100%;
  height: 100vh;
  padding: 3rem;
}

.unggulan-layout {
  height: 100%;
  display: grid;
  grid-template-rows: repeat(2, 1fr);
}

.unggulan-image-container {
  width: 100%;
  height: 100%;
  border-radius: 16px;
  overflow: hidden;
}

.unggulan-image-container img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.items {
  width: 100%;
  position: relative;
}

.item-container {
  width: 100%;
  aspect-ratio: 4 / 3;
  max-width: 500px;
  position: relative;
  padding: 1em;
}

.item-background-image-container {
  position: relative;
  width: 100%;
  height: 100%;
  border-radius: 16px;
  overflow: hidden;
}

.item-background-image {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}

.item-background-image img {
  width: 100%;
  height: 100%;
  filter: brightness(75%);
}

.item-title {
  position: absolute;
  bottom: 0;
  left: 0;

  width: 100%;
  padding: 1em;

  font-weight: bold;
  color: white;
  font-size: 1.25rem;

  background: linear-gradient(transparent, rgba(0, 0, 0, 0.7));
}

.maps {
  width: 100%;
  height: 50vh;
  display: flex;
  justify-content: center;
  margin-top: 2rem;
}

.contact-form-section {
  width: 100%;
  padding: 2rem 1rem 4rem;
  display: flex;
  justify-content: center;
}

.contact-form-card {
  width: min(720px, 100%);
  background: #fff;
  border: 1px solid #f1f1f1;
  border-radius: 20px;
  box-shadow: 0 18px 40px rgba(0, 0, 0, 0.08);
  padding: 2rem;
}

.contact-form-header {
  margin-bottom: 1.5rem;
}

.contact-form-header h2 {
  margin: 0 0 0.5rem;
  color: #111827;
  font-size: clamp(1.5rem, 2vw, 2rem);
}

.contact-form-header p {
  margin: 0;
  color: #4b5563;
  line-height: 1.6;
}

.contact-form {
  display: grid;
  gap: 1.25rem;
}

.contact-field {
  display: grid;
  gap: 0.5rem;
  color: #111827;
  font-weight: 600;
}

.contact-field input,
.contact-field textarea {
  width: 100%;
  border: 1px solid #d1d5db;
  border-radius: 12px;
  padding: 0.9rem 1rem;
  font: inherit;
  color: #111827;
  background: #fff;
  transition:
    border-color 0.2s ease,
    box-shadow 0.2s ease;
}

.contact-field input:focus,
.contact-field textarea:focus {
  outline: none;
  border-color: #dc2626;
  box-shadow: 0 0 0 3px rgba(220, 38, 38, 0.12);
}

.contact-field textarea {
  resize: vertical;
  min-height: 140px;
}

.mailto-button {
  margin-top: 1.5rem;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 0.5rem;
  width: 100%;
  padding: 0.9rem 1.25rem;
  border-radius: 12px;
  background: linear-gradient(135deg, #dc2626, #b91c1c);
  color: white;
  font-weight: 700;
  text-decoration: none;
  transition:
    transform 0.2s ease,
    box-shadow 0.2s ease;
  box-shadow: 0 16px 28px rgba(220, 38, 38, 0.18);
}

.mailto-button:hover {
  transform: translateY(-1px);
  box-shadow: 0 20px 30px rgba(220, 38, 38, 0.22);
}

.mailto-button i {
  font-size: 1.1rem;
}

@media (max-width: 640px) {
  .contact-form-card {
    padding: 1.25rem;
  }
}
</style>
