<template>
  <div>
    <nav class="navbar navbar-expand-md navbar-dark bg-dark mb-4">
      <div class="container-fluid">
        <ul class="navbar-brand logo">MUKELLEF</ul>

        <div class="d-flex">
          <ul class="navbar-nav me-auto mb-2 mb-md-0" >
            <li @click="submit" class="nav-item">
              <a  href="#" class="nav-link">Logout</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>

    <main class="form-signin">
      <Nuxt/>
    </main>
  </div>
</template>

<script>
export default {
  name: 'layout',

  methods: {
    submit() {
      this.$router.push('/');
    }
  }
}
</script>

<style>
.form-signin {
  width: 100%;
  max-width: 330px;
  padding: 15px;
  margin: auto;
}
.logo {
  font-size: 32px;
  margin: 0;
  padding: 0;

}

.form-signin .checkbox {
  font-weight: 400;
}

.form-signin .form-control {
  position: relative;
  box-sizing: border-box;
  height: auto;
  padding: 10px;
  font-size: 16px;
}

.form-signin .form-control:focus {
  z-index: 2;
}

.form-signin input[type="email"] {
  margin-bottom: -1px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}

.form-signin input[type="password"] {
  margin-bottom: 10px;
  border-top-left-radius: 0;
  border-top-right-radius: 0;
}
</style>
