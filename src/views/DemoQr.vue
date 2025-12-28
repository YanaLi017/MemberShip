<template>
  <button class="gcash-btn" @click="openGCash">
    Open in GCash App
  </button>
</template>
<script setup>
const gcashNumber = '09915134467'

const openGCash = () => {
  // GCash deep link (opens app if installed)
  const gcashAppLink = 'gcash://'

  // Fallback (web)
  const gcashWebLink = 'https://www.gcash.com'

  // Try opening app
  window.location.href = gcashAppLink

  // Fallback after 1.5s
  setTimeout(() => {
    window.location.href = gcashWebLink
  }, 1500)
}
</script>
