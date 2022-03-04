<template>
  <div class="container">
    <p v-if="$auth.loggedIn">Name：{{ $auth.user.name }}</p>

    <button v-on:click="getUser">APIを叩く</button>


  </div>
</template>

<script>
export default {
  data() {
  },
  methods: {
    async getUser() {
      try {
        const res = await this.$axios.get("http://localhost/api/auth/user", {
        });
        console.log(res);
      } catch (e) {
        console.error(e)
      }
    },
  },
};
</script>