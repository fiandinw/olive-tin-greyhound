<script setup>
import { ref } from 'vue'

const isMenuOpen = ref(false)

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
}

const closeMenu = () => {
  isMenuOpen.value = false
}
</script>

<template>
  <header>
    <div class="inner-header">
      <div class="logo-wrapper">
        <img alt="Vue logo" class="logo" src="@/assets/TSM-jukebox-bg-removed.png" />
      </div>

      <div class="listing-wrapper">
        <button
          type="button"
          class="menu-toggle"
          aria-label="Toggle menu"
          :aria-expanded="isMenuOpen"
          @click="toggleMenu"
        >
          <span class="listing-inner">
            <span class="icon-wrapper">
              <i class="icon bi bi-list"></i>
            </span>
          </span>
        </button>

        <Transition name="menu-fade">
          <nav v-if="isMenuOpen" class="menu-panel" @click="closeMenu">
            <a href="#beranda" class="menu-item" @click.prevent>Beranda</a>
            <a href="#produk-tsm" class="menu-item">Produk TSM</a>
            <a href="#" class="menu-item" @click.prevent>Tentang TSM</a>
            <a href="#keunggulan-tsm" class="menu-item" @click.prevent>Keunggulan TSM</a>
            <a href="#kontak" class="menu-item">Kontak</a>
          </nav>
        </Transition>
      </div>
    </div>
  </header>
</template>

<style scoped>
header {
  height: 70px;
  background-color: #fff;
  position: relative;
}
.inner-header {
  position: relative;
  display: flex;
  justify-content: space-between;
  height: 100%;
  padding: 0 1rem;
}
.logo-wrapper {
  background-color: red;
  width: 70px;
  height: 100%;
}
.logo {
  width: 100%;
  height: 100%;
  object-fit: contain;
  filter: brightness(900%);
}
.listing-wrapper {
  position: relative;
  width: 70px;
  height: 100%;
  padding: 0.75rem 0;
}
.menu-toggle {
  width: 100%;
  height: 100%;
  padding: 0;
  border: none;
  background: transparent;
  cursor: pointer;
}
.listing-inner {
  background-color: red;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%;
  width: 100%;
}
.icon-wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%;
}
.icon {
  font-size: 2.5rem;
  color: #fff;
}
.menu-panel {
  position: absolute;
  right: 0;
  top: calc(100% + 0.5rem);
  display: flex;
  flex-direction: column;
  min-width: 160px;
  padding: 0.5rem;
  background: #fff;
  border: 1px solid #f0f0f0;
  border-radius: 0.5rem;
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.12);
  z-index: 10;
  transform-origin: top right;
}
.menu-item {
  padding: 0.75rem 1rem;
  color: #333;
  text-decoration: none;
  border-radius: 0.375rem;
  transition: background-color 0.2s ease;
}
.menu-item:hover {
  background-color: #f5f5f5;
}

.menu-fade-enter-active,
.menu-fade-leave-active {
  transition:
    opacity 0.2s ease,
    transform 0.2s ease;
}

.menu-fade-enter-from,
.menu-fade-leave-to {
  opacity: 0;
  transform: translateY(-8px) scale(0.98);
}

.menu-fade-enter-to,
.menu-fade-leave-from {
  opacity: 1;
  transform: translateY(0) scale(1);
}
</style>
