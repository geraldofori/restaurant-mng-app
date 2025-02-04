<template>
  <div>
    <img class="logo" src="../assets//app-logo.webp" alt="" />
    <h1>Sign Up</h1>
    <div class="register">
      <input type="text" v-model="name" placeholder="Enter name" />
      <input type="email" v-model="email" placeholder="Enter email" />
      <input type="password" v-model="password" placeholder="Enter password" />
      <button v-on:click="signUp">Sign up</button>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "SignUp",
  data() {
    return {
      name: "",
      email: "",
      password: "",
    };
  },
  methods: {
    async signUp() {
      let result = await axios.post("http://localhost:3000/users", {
        email: this.email,
        password: this.password,
        name: this.name,
      });
      if (result.status == 201) {
        alert("Sign up successful!");
        localStorage.setItem("user-data", JSON.stringify(result.data));
      }
    },
  },
};
</script>

<style>
.logo {
  width: 100px;
}
.register input {
  width: 300px;
  height: 40px;
  padding-left: 20px;
  display: block;
  margin-bottom: 30px;
  margin-right: auto;
  margin-left: auto;
  border: 1px solid skyblue;
  border-radius: 8px;
}
.register button {
  width: 250px;
  height: 35px;
  border: 1px solid skyblue;
  background: skyblue;
  cursor: pointer;
  color: white;
}
</style>
