<template>
  <v-container>
    <v-layout text-center>
      <v-flex xs-12>
        <v-btn @click="authenticate" v-if="!isTokenPresent" large color="primary">Войти</v-btn>
        <div v-else>You are authorized</div>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      token: '',
      isTokenPresent: false
    }
  },
  mounted() {
    const token = window.localStorage.getItem('access_token');
    if (token) {
      this.token = token;
      this.isTokenPresent = true;
    }
  },
  methods: {
    async authenticate() {
      fetch('http://localhost:3000/authenticate')
      .then(r => r.json())
      .then(r => window.location.href = r.url);
    }
  }
};
</script>
