<template>
  <div class="col-md-3 profile-navbar">
    <ul class="nav nav-pills nav-stacked">
      <li class="active"><a href="#">Home</a></li>
      <li><a href="#">Menu 1</a></li>
      <li><a href="#">Menu 2</a></li>
      <li><a href="#">Menu 3</a></li>
    </ul>
  </div>
</template>

<style>
.profile-navbar {
  display: block;
}
</style>

<script lang="ts">
import { Vue, Component } from "@/utils/vue-imports";

@Component({
  name: "Navbar",
})
export default class Navbar extends Vue {}
</script>
