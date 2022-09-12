<template>
  <div>
    <form @submit.prevent="submit" id="form" name="form">
        <h1 class="h3 mb-3 fw-normal">Please sign in</h1>
        <p class="hint">admin admin</p>
        <input v-model="name" type="name" class="form-control" placeholder="name" required>
        <input v-model="password" type="password" class="form-control" placeholder="Password" required>
        <span > {{ message }}</span>
        <button class="w-100 btn btn-lg btn-primary" type="submit">Sign in</button>
    </form>

  </div>
</template>

<script>

export default {
  data() {
    return {
      name: '',
      password: '',
      message:''
    }
  },
  methods: {

    submit() {

      if(this.name == 'admin' && this.password == 'admin'){
        this.$router.push('/logged');
      }
      else {
        this.$el.querySelector("span").innerText = 'admin, admin ';
      }
      if(this.name !== 'admin' && this.password == 'admin') {
        this.$el.querySelector("span").innerText = 'admin yazmayı dene bence';
      }
      if(this.name == 'admin' && this.password !== 'admin') {
        this.$el.querySelector("span").innerText = 'şifreye de admin yazmayı dene bence';
      }

    }
  }
}
</script>

<style scoped>
  .hint {
    font-size: 10px;
    color: #999;
    margin: 0;
    padding: 0;
  }
</style>
