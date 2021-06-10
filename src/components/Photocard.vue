<template>
  <!-- <div class="col-sm-6 col-lg-4"> -->
  <div class="photocard card">
    <img class="card-img" :src="imgpath" :alt="imgpath" />
    <div class="card-img-overlay">
      <h5 class="card-title"></h5>
      <!-- <p class="card-text">hallo</p> -->
      <p class="card-text"></p>
    </div>
  </div>
  <!-- </div> -->
</template>

<style>
.photocard {
  padding: 0;
  margin: 0;
  border-color: black;
}
</style>

<script lang="ts">
import { Vue, Component } from "@/utils/vue-imports";

const photocardProps = Vue.extend({
  props: {
    imgpath: String,
  },
});

@Component
export default class Photocard extends photocardProps {
  data() {
    return this.imgpath;
  }
}
</script>
