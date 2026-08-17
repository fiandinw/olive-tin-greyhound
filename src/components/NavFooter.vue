<script setup>
defineProps({
  msg: {
    type: String,
    required: true,
  },
})
</script>

<template>
  <footer>
    <div class="inner-footer">
      <div class="footer-content">
        <div class="footer-logo-wrapper">
          <img alt="Vue logo" class="footer-logo" src="@/assets/TSM-jukebox-bg-removed.png" />
        </div>
        <div class="footer-text-wrapper">
          <p>© 2026 Trimagna Sinergi Makmur. All rights reserved.</p>
        </div>
      </div>
    </div>
  </footer>
</template>

<style scoped>
footer {
  width: 100%;
  height: 70px;
  background-color: black;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  flex-shrink: 0;
}

.inner-footer {
  width: 100%;
  height: 100%;
  padding: 0 1rem;
  box-sizing: border-box;

  display: flex;
  justify-content: center;
  align-items: center;
}

.footer-content {
  height: 100%;
  display: flex;
  align-items: center;
  gap: 1rem;
}

.footer-logo-wrapper {
  width: 70px;
  height: 70px;
  background-color: red;
  flex-shrink: 0;
}

.footer-logo {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: contain;
  filter: brightness(900%);
}

.footer-text-wrapper {
  color: white;
  font-size: 0.875rem;
}

.footer-text-wrapper p {
  margin: 0;
}
</style>
