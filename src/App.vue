<template>
  <div class="login-container">
    <div class="login-image"></div>
    <div class="login-form">
      <h2>Hoş Geldiniz</h2>
      <br>
      <div class="form-group">
        
        <label for="username">Kullanıcı Adı:</label>
        <input type="text" id="username" v-model="username" placeholder="kullanici-adi" />
      </div>
      <div class="form-group">
        <label for="password">Şifre:</label>
        <input type="password" id="password" v-model="password" placeholder="password" />
      </div>
      <button @click="login">Giriş Yap</button>
      <br> <br>

        <a href="/accounts/password/reset/" :color="black" class="formcontrol">Şifreni mi unuttun?</a>
        <br>
        <div class="stylee">
<h3 class="h3 font-weight-bold">Sosyal Ağlar ile Giriş Yap</h3>

<div class="d-flex socials-buttons">

<a href="...."  style="color: blue; " title="Linkedin">
  <i class="fab fa-linkedin-in" aria-hidden="true" style="transform: scale(1.8);"></i>
</a>

<a href="/accounts/google/login/" title="Google" style="color: red; ; margin-left: 20px; margin-right: 20px;">
  <i class="fab fa-google" aria-hidden="true" style="transform: scale(1.8);"></i>
</a>


<a href="..." title="Github" style="color: black; " >
<i class="fab fa-github" aria-hidden="true" style="transform: scale(1.8);"></i>
</a>


</div>
<br>
<hr>
<h4 class="h3 font-weight-bold">Kayıtlı değil misin?

<a href="/kayitol" class="small font-weight-bold" style="color: #151d35;">Hemen kaydol!</a>
</h4>

</div>

    </div>
  </div>
</template>

<script>
module.exports = {
  data() {
    return {
      username: '',
      password: ''
    };
  },
  methods: {
    login() {
      // Giriş işlemleri burada yapılabilir
      console.log('Kullanıcı Adı:', this.username);
      console.log('Şifre:', this.password);
    }
  }
};
</script>

<style>
body {
  margin: 0;
  padding: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: #f46f4e;
}
.socials-buttons {
  
  display: flex; 
  justify-content: center; 
  align-items: center;
  
}

.stylee{
    color: #000000;
  align-items: center;
  justify-content: center;
  font-weight: 800; 
  font-weight: bold; 
  text-align: center; 
  margin-top: 20px; 
}

.login-container {
  display: flex;
  width: 700px;
  height: 550px;
  background-color: white;
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.login-image {
  flex: 1;
  background: url('logo.png') center/cover;
  height: 400px;
  margin-top: 55px;
}

.login-form {
  flex: 1;
  padding: 20px;
  box-sizing: border-box;
  margin-top: 100px;
}

.form-group {
  margin-bottom: 20px;
}
.formcontrol{
  color: #000000;
  opacity: 0.7;
  font-weight:100;
font-weight:800;
font-weight:bold;
float: right;
margin-bottom: 10px;
}

label {
  display: block;
  margin-bottom: 8px;
  font-weight: bold;
}

input {
  width: 100%;
  padding: 8px;
  border: 1px solid #ccc;
  border-radius: 4px;
}

button {
  width: 100%;
  padding: 10px;
  background-color: rgb(192, 43, 43);
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}
h2{
margin-top: -50px;
}

button:hover {
  background-color: rgb(211, 65, 65);
}
</style>
