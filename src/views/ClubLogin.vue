<script setup>
import { useRouter } from 'vue-router';
const router = useRouter();
const signUp = () => {
  router.push({ name: 'clubsignup' });
};
</script>

<template>

  <main>
    <div>
      <img src="@/assets/logo.png" alt="Logo" id="logo">
    </div>
    <div class="card">
      <h1>Club Login</h1>

      <div class="form">
        <input type="text" placeholder="Club ID">
        <input type="text" placeholder="Password">
      </div>

      <div class="rememberMe">

        <label class="container">Remember me
          <input type="checkbox" checked="checked">
          <span class="checkmark"></span>
        </label>

        <label>
          <a href="#" id="forgotPassword">Forgot Password?</a>
        </label>
      </div>

      <div class="login">
        <button id="loginBtn">Login</button>
      </div>
      
      <div>
        <span id="signup">Not a member yet? <button id="signupbtn" @click="signUp">Sign up</button></span>
      </div>

    </div>
  </main>
</template>



<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

* {
  font-family: 'Poppins', sans-serif;
}

main {
  background-image: url('@/assets/bg .jpg');
  width: 100dvw;
  height: 100dvh;
  background-size: cover;
  background-position: center;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

.card {
  width: 30rem;
  height: 30rem;
  background-color: rgba(255, 255, 255, 0.4);
  backdrop-filter: blur(5px);
  display: flex;
  flex-direction: column;
  align-items: center;
  border-radius: 20px;
  padding-top: 50px;
}

.card h1 {
  font-size: 30px;
  margin-bottom: 20px;
  color: #214444;
  font-weight: 600;
}

.form {
  display: flex;
  flex-direction: column;
  gap: 20px;
  margin-top: 20px;
}

.form input {
  width: 350px;
  height: 40px;
  padding: 10px;
  border: none;
  border-radius: 10px;
  font-size: 15px;
}

.container {
  display: block;
  position: relative;
  padding-left: 25px;
  cursor: pointer;
  font-size: 13px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  color: #214444;
  margin-top: 10px;
}

/* Hide the browser's default checkbox */
.container input {
  position: absolute;
  opacity: 0;
  cursor: pointer;
  height: 10px;
  width: 10px;
}

.checkmark {
  position: absolute;
  top: 0;
  left: 0;
  height: 15px;
  width: 16px;
  background-color: #8CADA9;
  border-radius: 3px;
}

.container:hover input~.checkmark {
  background-color: #659399;
}

.container input:checked~.checkmark {
  background-color: #214444;
}

.checkmark:after {
  content: "";
  position: absolute;
  display: none;
}

.container input:checked~.checkmark:after {
  display: block;
}

.container .checkmark:after {
  left: 5px;
  top: 2px;
  width: 7px;
  height: 10px;
  border: solid #708C8A;
  border-width: 0 3px 3px 0;
  -webkit-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  transform: rotate(45deg);
}

.rememberMe {
  display: flex;
  justify-content: space-between;
  width: 350px;
  align-items: center;
  margin-top: 10px;
}

.rememberMe a {
  text-decoration: none;
  color: #214444;
  font-size: 13px;
}

#forgotPassword:hover {
  text-decoration: underline;
  cursor: pointer;
}

.login {
  margin-top: 30px;
}
#loginBtn {
  width: 150px;
  height: 40px;
  border: none;
  border-radius: 10px;
  background-color: #214444;
  color: white;
  font-size: 18px;
  cursor: pointer;
}
#loginBtn:hover {
  background-color: #659399;
}
#signupbtn{
  background-color: transparent;
  border: none;
  cursor: pointer;
  color: #214444;
  margin-top: 20px;
  font-size: 13px;
}
#signupbtn:hover {
  text-decoration: underline;
}
#signup {
  font-size: 13px;
}
</style>
