<template>
  <div class="entry-title d-flex justify-content-between p-2">
    <div>
      <span class="text-success fs-3 fw-bold">14</span>
      <span class="mx-1 fs-3">Diciembre</span>
      <span class="mx-2 fs-4 fw-light">1992, Lunes</span>
    </div>
    <div>
      <button class="btn btn-danger mx-2">
        Borrar
        <i class="fa-solid fa-trash"></i>
      </button>
      <button class="btn btn-primary">
        Subir Foto
        <i class="fa-solid fa-upload"></i>
      </button>
    </div>
  </div>
  <hr />
  <div class="d-flex flex-column px-3 h-75">
    <textarea placeholder="¿Qué sucedió hoy?"></textarea>
  </div>
  <Fab icon="fa-floppy-disk" />
  <img
    src="https://s1.1zoom.me/big0/735/Germany_Mountains_Sunrises_and_sunsets_Houses_568280_1280x853.jpg"
    alt="Entry Picture"
    class="img-thumbnail"
  />
</template>

<script>
import { defineAsyncComponent } from "@vue/runtime-core";
export default {
  components: {
    Fab: defineAsyncComponent(() => import("../components/Fab.vue")),
  },
};
</script>

<style lang="scss" scoped>
textarea {
  font-size: 20px;
  border: none;
  height: 100%;

  &:focus {
    outline: none;
  }
}
img {
  width: 200px;
  position: fixed;
  bottom: 100px;
  right: 20px;
  box-shadow: 0px 5px 10px rgba($color: #000000, $alpha: 0.2);
}
</style>