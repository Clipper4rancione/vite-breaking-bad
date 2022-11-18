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
    <div class="select-cast d-flex">
      <select v-model="store.categorySwap" class="form-select">
        <option @click="$emit('startFilter')" value="" selected>Select category</option>
        <option @click="$emit('startFilter')" value="Breaking Bad">Breaking Bad</option>
        <option @click="$emit('startFilter')" value="Better Call Saul">Better Call Saul</option>
      </select>
    </div>
    <div class="container mc-container">
      <div class="founded p-3 text-center">
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
  margin: 30px 0px;
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