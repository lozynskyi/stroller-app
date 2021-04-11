<template>
  <form @click.prevent="login">
    <button type="submit">Login</button>
  </form>
</template>

<script>
export default {
  methods: {
    login() {
      this.$auth.loginWith('laravelSanctum', {
        data: {
          email: 'valera@gmx.com',
          password: 'password'
        }
      })
    }
  }
}
</script>
