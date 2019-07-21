<template>
  <div class="dropper">
    <input type="file" @change="uploadImages($event.target.files)" multiple accept="image/*" />
    <span class="ui header">Drag files here!</span>
  </div>
</template>

<script>
import { mapActions } from "vuex";

export default {
  name: "UploadForm",
  methods: {
    ...mapActions(["uploadImages"])
  }
};
</script>

<style scoped>
.dropper {
  height: 30vh;
  border: 2px dashed black;
  border-radius: 10px;
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
}
.dropper:hover {
  background-color: #eee;
}
.dropper input {
  width: 100%;
  height: 100%;
  position: absolute;
  opacity: 0;
}
</style>
