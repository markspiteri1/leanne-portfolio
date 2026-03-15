<template>
  <div class="app-container">
    <Navbar />
    <main class="main-content">
      <NuxtLayout>
        <NuxtPage />
      </NuxtLayout>
    </main>
    <Footer />
  </div>
</template>

<script setup>
useHead({
  title: 'Leanne Lewis'
})
</script>

<style>
.app-container {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

.main-content {
  flex: 1;
  padding-top: 6rem;
}
</style>
