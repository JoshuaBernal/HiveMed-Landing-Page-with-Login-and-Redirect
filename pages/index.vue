<template>
  <div>
    <div>
      <div class="main-top">
        <nav class="nav-bar">
          <div class="name-logo">
              <img src="/profil.png" alt="profil" width="55" class="logo-img">
              <p class="logo-name">HiveMed</p>
          </div>

          <div>
              <a href="#overview" class="overview">Overview</a>
          </div>

          <div class="buttons">
              <button @click="ToReg" class="btn-reg">Register</button>
              <button @click="ToLogin" class="btn-log">Login</button>
          </div>
        </nav>
        <p id="overview" class="above-header">A New Way To Experience Health Care</p>
        <div class="ov-width">
        <div class="overview-main">
          <img src="/socialmedia.png" alt="" class="graphics">
            
          <p class="header">Where Health Care Meets Social Media</p>
          <p class="subheader">A social hub that connects patients, doctors, and pharmacies all in one place. </p>
        </div>
      </div>
        <div class="ov-buttons">
              <button class="btn-start">Get Started</button>
              <button class="btn-hiw">Watch How it Works</button>
        </div>
      </div>
    </div>
  </div>

<!--FOOTER-->
<div class="Footer">
  <div class="top-footer">
      <div>
          <p class="foothead">ALTERNATIVES</p>
        <div>
          <p class="mt-4">Buffer</p>
          <p class="mt-4">eMARs</p>
          <p class="mt-4">EMRs</p>
          <p class="mt-4">EHRs</p>
        </div>
      </div>

      <div>
          <p class="foothead">SITEMAP</p>

        <div>
          <p class="mt-4">Overview</p>
          <p class="mt-4">How It Works</p>
          <p class="mt-4">Features</p>
          <p class="mt-4">Benefits</p>
          <p class="mt-4">Login or Register</p>
        </div>
      </div>

      <div>
          <p class="foothead">HYPEX</p>

        <div>
          <p class="mt-4">About Us</p>
          <p class="mt-4">Contact</p>
          <p class="mt-4">Privact Policy</p>
          <p class="mt-4">Term of Service</p>
          <p class="mt-4">Help</p>
        </div>
      </div>      

      <div>
          <p class="foothead">GET IN TOUCH</p>

        <div>
          <p class="mt-4">Twitter</p>
          <p class="mt-4">Facebook</p>
          <p class="mt-4">Github</p>
          <p class="mt-4">Dribble</p>
        </div>
      </div>
  </div>
  <p class="bot-footer">COPYRIGHT © 2022 — DESIGN NAUVAL — SLICING ARIE</p>
</div>
</template>
  
  <script>
  export default {
    methods: {
      ToLogin() {
        this.$router.push('/login');
      },
      ToReg() {
        this.$router.push('/signup');
      },
    },
  }
  </script>

  <script setup>
  useHead({
    title: 'Dashboard'
  })
</script>
  
<style>
.nav-bar {
  display: flex;
  justify-content: space-between;
  margin: none;
  background-color: #00022D;
  color: white;
  padding: 45px;
}
.overview {
  text-align: center;
  font-family: 'DM Sans', sans-serif;
  color: white;
  font-weight: bold;
  text-decoration: none;
  font-size: 16px;
  line-height: 70px;
}
.buttons {
  margin-right: 10px;
  line-height: 70px;
}
.btn-reg {
  background: none;
  color: white;
  border: 0px;
  font-weight: bold;
  font-size: 16px;
  font-family: 'DM Sans', sans-serif;
  margin-right: 24px;
  cursor: pointer;
}
.btn-log {
  background: white;
  border: 0px;
  font-family: 'DM Sans', sans-serif;
  font-weight: bold;
  font-size: 16px;
  padding-left: 16px;
  padding-right: 16px;
  padding-top: 12px;
  padding-bottom: 12px;
  border-radius: 20px;
  cursor: pointer;
}
.name-logo {
  display: flex;
  justify-content: flex-start;
}
.logo-name {
  font-family: 'Source Sans Pro', sans-serif;
  font-weight: 600;
  font-size: 1.25rem;
  line-height: 1.75rem;
  margin-left: 0.75rem;
}
.logo-img {
  line-height: inherit;
  -webkit-text-size-adjust: 100%;
  width: 55px;
  height: 55px;
}
.main-top {
  background-color: #00022D;
  margin: 0px;
  height: 950px;
}
.graphics {
  display: block;
  width: 73%;
  margin-top: 10px;
  margin-left: auto;
  margin-right: auto;
}
.overview-main {
  display: block;
  position: relative;
}
.overview-main p{
  position: absolute;
  bottom: 0;
  right: 0;
  left: 0;
  top: 0; 
}
.above-header {
  color: #fc881d;
  background-color: none;
  font-family: 'DM Sans', sans-serif;
  font-weight: bold;
  font-size: 1.125rem;
  line-height: 1;
  text-align: center;
}
.header {
  color: white;
  background-color: none;
  font-family: 'Source Sans Pro', sans-serif;
  font-weight: normal;
  padding-top: 100px;
  
  font-size: 48px;
  line-height: 1;
  text-align: center;
}
.subheader {
  color: white;
  background-color: none;
  font-family: 'DM Sans', sans-serif;
  font-weight: bold;
  font-size: 18px;
  text-align: center;
  padding-top: 200px;
}
.overview-main button {
  position: absolute;
}
.ov-buttons {
  display: flex;
  justify-content: center;
}
.btn-start {
  background-color: #fc881d;
  color: white;
  font-size: 16px;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif, sans-serif;
  font-weight: bold;
  border-radius: 900px;
  padding-left: 20px;
  padding-right: 20px;
  padding-top: 12px;
  padding-bottom: 12px;
  margin-right: 10px;
  cursor: pointer;
  border: 0px;
}
.btn-hiw {
  background: none;
  color:white;
  margin-left: 10px;
  border: none;
  font-size: 16px;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  padding-left: 20px;
  padding-right: 20px;
  padding-top: 12px;
  padding-bottom: 12px;
  font-weight: bold;
  cursor: pointer
}
body {
  margin: 0px;
}
.top-footer {
  display: flex;
  justify-content: space-evenly;
}
.bot-footer {
  text-align: center;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  font-weight: bold;
  font-size: 16px;
  padding-top: 60px;
}
.foothead {
  text-align: left;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  font-weight: bold;
  font-size: 14px;
}
.mt-4 {
  text-align: left;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  font-weight: normal;
  font-size: 16px;
}
.Footer {
  height: 400px;
  padding-top: 100px;
}
</style>