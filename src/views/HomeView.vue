<script setup></script>

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
</style>
