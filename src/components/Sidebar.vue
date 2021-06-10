<template>
  <div class="profile-info col-md-4 col-lg-2">
    <div class="profile-text-container">
      <h1 class="profile-text-title text-uppercase initialism">
        <small width="70%;">Hanalei Ezz</small>
      </h1>
      <h4 class="profile-text-description initialism text-lowercase">
        <small>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
          minim veniam, quis nostrud exercitation ullamco laboris nisi ut
          aliquip ex ea commodo consequat. Duis aute irure dolor in
          reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla
          pariatur. Excepteur sint occaecat cupidatat non proident, sunt in
          culpa qui officia deserunt mollit anim id est laborum.
        </small>
      </h4>
      <div class="profile-navbar">
        <Navbar />
      </div>
    </div>
  </div>
</template>

<style>
.profile-info {
  background-image: linear-gradient(#080808, #1a1b1b);
}

.profile-text-title {
  display: inline-block;
}

.profile-text-container {
  width: 95%;
  margin: 15% 0 5%;
  padding: 3.5%;
  color: antiquewhite;
}

/* .profile-text-description {
} */
</style>

<script lang="ts">
import { Vue, Component } from "@/utils/vue-imports";

@Component({
  name: "Sidebar",
})
export default class Sidebar extends Vue {}
</script>
