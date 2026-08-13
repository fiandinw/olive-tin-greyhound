<script setup>
defineProps({
  msg: {
    type: String,
    required: true,
  },
})
</script>

<template>
  <header>
    <div class="inner-header">
      <div class="logo-wrapper">
        <img alt="Vue logo" class="logo" src="@/assets/TSM-jukebox-bg-removed.png" />
      </div>
      <div class="listing-wrapper">
        <div class="listing-inner">
          <div class="icon-wrapper">
            <i class="icon bi bi-list"></i>
          </div>
        </div>
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
  width: 70px;
  height: 100%;
  padding: 0.75rem 0;
}
.listing-inner {
  background-color: red;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%;
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
</style>
