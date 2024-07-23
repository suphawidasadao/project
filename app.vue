<template>
  <div class="register-page">
  <h1>T-POP Hub</h1>
  <form @submit.prevent="register">
  <div class="form-group">
  <label for="username">ชื่อผู้ใช้</label>
  <input type="text" id="username" v-model="form.username" required />
  </div>
  <div class="form-group">
  <label for="fullname">ชื่อ-สกุล</label>
  <input type="text" id="fullname" v-model="form.fullname" required />
  </div>
  <div class="form-group">
  <label for="email">อีเมล</label>
  <input type="email" id="email" v-model="form.email" required />
  </div>
  <div class="form-group">
  <label for="password">รหัสผ่าน</label>
  <input type="password" id="password" v-model="form.password" required />
  </div>
  <div class="form-group">
  <label for="confirmPassword">รหัสผ่านยืนยัน</label>
  <input type="password" id="confirmPassword" v-model="form.confirmPassword" required />
  </div>
  <button type="submit">สร้างบัญชี</button>
  <button type="button" @click="login">ล็อกอิน</button>
  </form>
  </div>
  </template>
  <script>
  export default {
  data() {
     return {
       form: {
         username: '',
         fullname: '',
         email: '',
         password: '',
         confirmPassword: '',
       },
     };
  },
  methods: {
     register() {
       console.log('Registering user', this.form);
     },
     login() {
       console.log('Navigating to login page');
     },
  },
  };
  </script>
  <style scoped>
  .register-page {
  background-color: #f0f;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
  font-family: Arial, sans-serif;
  }
  h1 {
  color: white;
  }
  form {
  display: flex;
  flex-direction: column;
  background-color: white;
  padding: 2rem;
  border-radius: 8px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  }
  .form-group {
  margin-bottom: 1rem;
  }
  label {
  margin-bottom: 0.5rem;
  color: #333;
  }
  input {
  padding: 0.5rem;
  border: 1px solid #ccc;
  border-radius: 4px;
  }
  button {
  padding: 0.5rem;
  margin-top: 1rem;
  border: none;
  border-radius: 4px;
  color: white;
  background-color: #007bff;
  cursor: pointer;
  }
  button[type="button"] {
  background-color: #6c757d;
  }
  </style>