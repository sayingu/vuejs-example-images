<template>
  <div class="ui four cards">
    <div class="card" v-for="image in allImages" :key="image.id">
      <div class="image">
        <img :src="image.link" />
      </div>
    </div>
  </div>
</template>

<script>
import { mapGetters, mapActions } from "vuex";

export default {
  name: "ImageList",
  computed: { ...mapGetters(["allImages"]) },
  methods: { ...mapActions(["fetchImages"]) },
  created() {
    this.fetchImages();
  }
};
</script>
