<script setup>
import Navbar from "../components/Navbar.vue";
import Accordion from "../components/Accordion.vue";
</script>

<template>
  <body>
  <Navbar></Navbar>

  <main>
    <div class="sidebar">
      <Accordion/>
    </div>

  </main>
  </body>
</template>

<style>
body{
  background-image: url("../assets/bgquran3.jpg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  height: 800px;
}
.sidebar{
  padding: 20px;
  float: right;
  width: 40%;
}
</style>