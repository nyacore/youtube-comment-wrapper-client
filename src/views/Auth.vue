<template>
  
</template>

<script>
export default {
  async mounted() {
    window.localStorage.setItem('access_token', this.$route.params.token);
    this.$router.push({ name: 'home' });
  }
}
</script>