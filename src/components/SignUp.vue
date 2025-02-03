<template>
  <div>
    <img class="logo" src="../assets//app-logo.webp" alt="" />
    <h1>Sign Up</h1>
    <div class="register">
      <input type="text" placeholder="Enter name" />
      <input type="email" placeholder="Enter email" />
      <input type="password" placeholder="Enter password" />
      <button>Sign up</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "SignUp",
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
