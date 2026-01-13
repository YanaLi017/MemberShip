<template>
  <div class="datetime">
    <div class="time">{{ time }}</div>
    <div class="date">{{ date }}<br>(GMT +8)</div>
  </div>
</template>

<style scoped>
.datetime {
  text-align: center;
  font-family: 'Poppins', sans-serif;
  color: #214444;
}

.time {
  font-size: 2rem;
  font-weight: bold;
}

.date {
  font-size: 1.2rem;
  margin-top: 5px;
  font-weight: 500;
}
</style>

<script>
export default {
  data() {
    return {
      time: '',
      date: '',
      timer: null
    }
  },
  mounted() {
    this.updateDateTime()
    this.timer = setInterval(this.updateDateTime, 1000)
  },
  beforeUnmount() {
    clearInterval(this.timer)
  },
  methods: {
    updateDateTime() {
      const now = new Date()

      this.time = now.toLocaleTimeString('en-PH', {
        hour: '2-digit',
        minute: '2-digit',
        second: '2-digit'
      })

      this.date = now.toLocaleDateString('en-PH', {
        weekday: 'long',
        year: 'numeric',
        month: 'long',
        day: 'numeric'
      })
    }
  }
}
</script>
