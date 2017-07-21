<template>
<div class="content">
  <div class="has-text-centered">
    <h1 class="is-title is-bold">Register</h1>
  </div>

  <div class="columns">
    <div class="column is-6 is-offset-3">
      <div class="box">
        <div v-show="error" style="color:red; word-wrap:break-word;">{{ error }}</div>
        <form v-on:submit.prevent="register">
          <label class="label">Email</label>
          <p class="control">
            <input v-model="data.body.username" class="input" type="text" placeholder="email@example.org">
          </p>
          <label class="label">Company</label>
          <p class="control">
            <input v-model="data.body.company_name" class="input" type="text" placeholder="My Corp">
          </p>
          <label class="label">Name</label>
          <p class="control">
            <input v-model="data.body.username" class="input" type="text" placeholder="email@example.org">
          </p>
          <label class="label">Password</label>
          <p class="control">
            <input v-model="data.body.password" class="input" type="password" placeholder="password">
          </p>
          <label class="label">Confirm Password</label>
          <p class="control">
            <input v-model="data.body.password_confirmation" class="input" type="password" placeholder="password">
          </p>

          <hr>
          <p class="control">
            <button type="submit" class="button is-primary">Register</button>
          </p>
        </form>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  data () {
    return {
      data: {
        body: {
          username: null,
          password: null
        },
        rememberMe: false
      },
      error: null
    }
  },
  methods: {
    register () {

    }
  },
  beforeMount () {
    this.$store.state.app.sidebar.hidden = true
  }
}
</script>

<style lang="scss" scoped>
.is-title {
    text-transform: capitalize;
}
</style>
