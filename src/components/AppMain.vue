<script>
import { store } from "../data/store";
import ActorCard from "./ActorCard.vue";
export default {
  name: "AppMain",
  components: {
    ActorCard,
  },
  data() {
    return {
      store,
    };
  },
};
</script>

<template>
  <div class="container">
    <div class="select-cast">
      <select class="form-select">
        <option selected>Breaking Bad</option>
        <option value="1">Better Call Saul</option>
        <option value="2">El Camino</option>
      </select>
    </div>
    <div class="container mc-container">
      <div class="founded">
        <h3>Sono stati trovati {{ store.castList.length }} attori</h3>
      </div>
      <div class="container w-100">
        <div class="row p-2 d-flex justify-content-center">
          <ActorCard
            v-for="actor in store.castList"
            :actor="actor"
            :key="actor.id"
          />
        </div>
      </div>
    </div>
  </div>
</template>


<style lang="scss" scoped>
.select-cast {
  width: 15%;
  margin-top: 30px;
}
.mc-container {
  padding: 20px;
  background-color: white;
  width: 100%;
}
.founded {
  padding: 5px;
  margin: 0 auto;
  background-color: black;
  color: white;
}
</style>