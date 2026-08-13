<script setup></script>

<template>
  <main>
    <div class="banner-container">
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
            <button><i class="bi bi-whatsapp"></i> Hubungi Kami</button>
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
  background-color: #25d366;
  border: none;
  border-radius: 8px;
  padding: 0.75em 1.25em;

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
</style>
