<template>
  <div>
    Home
  </div>
</template>

<script>
export default {
  mounted() {
    this.$echo.channel('posts')
      .listen('PostCreated', (e) => {
        console.log(e)
      })
  },

  beforeRouteLeave(to, from, next) {
    this.$echo.leave('posts')
    next()
  }
}
</script>
