<template>
  <div
    class="outer-container container-fluid mh-100 d-flex p-0 flex-column text-center"
  >
    <div class="row-container row flex-grow-1 p-0">
      <Sidebar></Sidebar>
      <div class="portfolio-section col-md-8 col-lg-10 p-0">
        <masonry
          :cols="{ default: 2, 1900: 4, 1500: 3, 991: 2, 600: 1 }"
          :gutter="{ default: '1px', 1300: '0px' }"
        >
          <Photocard
            v-for="card in images"
            v-bind:imgpath="card.image"
            v-bind:key="card.id"
          ></Photocard>
        </masonry>
      </div>
    </div>
  </div>
</template>

<style>
.outer-container {
  position: absolute;
  height: 100%;
  width: 100%;
  overflow: hidden;
  display: block;
}

.row-container {
  position: absolute;
  top: 0;
  right: 0;
  height: 100%;
  margin: 0;
  width: 100%;
  overflow: hidden;
}

.portrfolio-section::-webkit-scrollbar {
  display: none;
}

/* width */
.portfolio-section::-webkit-scrollbar {
  width: 7px;
}

/* Track */
.portfolio-section::-webkit-scrollbar-track {
  background: #080808;
}

/* Handle */
.portfolio-section::-webkit-scrollbar-thumb {
  background: #888;
}

/* Handle on hover */
.portfolio-section::-webkit-scrollbar-thumb:hover {
  background: rgb(199, 199, 199);
}

.portfolio-section {
  height: 100%;
  display: block;
  background-image: linear-gradient(#080808, #0d0d0e);
  background-color: rgb(4, 4, 4);
  overflow-x: hidden;
  overflow-y: scroll;
}
</style>

<script lang="ts">
import { Vue, Component } from "@/utils/vue-imports";
import Sidebar from "@/components/Sidebar.vue";
import Photocard from "@/components/Photocard.vue";
import Navbar from "@/components/Navbar.vue";
import VueMasonry from "vue-masonry-css";

Vue.use(VueMasonry);

@Component({
  name: "Home",
  components: {
    Sidebar,
    Photocard,
    Navbar,
  },
})
export default class Home extends Vue {
  images = [
    { id: 0, image: "/img/lei_photography/ShoeUp.jpg" },
    { id: 1, image: "/img/lei_photography/FaceUpBrick.jpeg" },
    { id: 2, image: "/img/lei_photography/Daniel-Manny.jpg" },
    { id: 3, image: "/img/lei_photography/Summer-Spring.jpg" },
    { id: 4, image: "/img/lei_photography/BearBlackandBlue.JPG" },
    { id: 5, image: "/img/lei_photography/Lei-Asheville-Notgreatpic.jpg" },
    { id: 6, image: "/img/lei_photography/Summer-Beach.jpg" },
    { id: 7, image: "/img/lei_photography/Schmidty-Pink.jpg" },
    { id: 8, image: "/img/lei_photography/Lilly-Toy.jpg" },
    { id: 9, image: "/img/lei_photography/Lilly-Rainbow.jpg" },
    { id: 10, image: "/img/lei_photography/NG-Grayscale.jpg" },
  ];
}
</script>
