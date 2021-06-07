<template>
  <div class="text-center p-0 m-0 container-fluid">
    <div class="row">
      <Navbar />
    </div>
    <div class="row">
      <div class="col-md-4 col-lg-2" style="background-color: yellow;">
        <p>Lorem ipsum...</p>
      </div>
      <div class="photocard-container col-md-8 col-lg-10 mh-100" style="background-color: pink;">
        <div class="row" data-masonry='{"percentPosition": true }'></div>
          <Photocard
            v-for="card in images"
            v-bind:imgpath="card.image"
            v-bind:key="card.id"
          ></Photocard>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Vue, Component } from "@/utils/vue-imports";
import Navbar from "@/components/Navbar.vue";
import Photocard from "@/components/Photocard.vue";

@Component({
  name: "Home",
  components: {
    Navbar,
    Photocard,
  },
})
export default class Home extends Vue {
  // computed: {

  // },
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
