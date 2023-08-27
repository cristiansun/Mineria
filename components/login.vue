<template>
    <div class="login-container">
      <h1>Login</h1>
      <input v-model="username" type="text" placeholder="Ingrese el usuario">
      <input v-model="password" type="password" placeholder="Ingrese la contraseña">
      <button @click="login">Login</button>
      <p v-if="errorMessage" class="error-message">{{ errorMessage }}</p>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        username: "",
        password: "",
        errorMessage: ""
      };
    },
    methods: {
      login() {
        if (this.username === "admin" && this.password === "admin") {
          this.$router.push("/index");
        } else {
          this.errorMessage = "Credenciales incorrectas. Por favor, intenta nuevamente.";
        }
      }
    }
  };
  </script>
  
  <style scoped>
  .login-container {
    text-align: center;
    margin-top: 100px;
  }
  
  .error-message {
    color: red;
    margin-top: 10px;
  }
  </style>
  