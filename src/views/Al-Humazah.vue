<template>
  <Navbar></Navbar>
  <div class="about">
    <h1>Daftar Surah</h1>
    <ul>v-for="chapter in chapters" :key="chapter['id']">
      <li>
        <router-link to="{ name: 'Surah', params: { id: chapter['id'] } }">{{
        `${chapter["name_simple"]} (${chapter["name_arabic"]})`
          }}</router-link>
      </li>
    </ul>
  </div>
</template>
<script>
import Navbar from "../components/Navbar.vue";

export default {
  data() {
    return {
      components: { Navbar },
      chapters: []
    };
  },
  async mounted() {
    const response = await fetch(
      "https://api.quran.com/api/v4/chapters?language=id"
    ).then((res) => res.json());
    this.chapters = response["chapters"];
  },
  methods: {},
};
</script>
<style>
</style>
