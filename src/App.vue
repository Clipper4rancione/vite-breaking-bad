<script>
import axios from "axios";
import { store } from "./data/store";

import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";

export default {
  name: "App",
  data() {
    return {
      store,
    };
  },
  components: {
    AppHeader,
    AppMain,
  },
  methods: {
    getCharacters() {
     axios.get(store.apiUrlBrBa, {
      params:{
        category: store.categorySwap
      }
     })
     .then( result => {
      store.castList = result.data;
     })
     .catch( error => {
      console.log(error);
     })
    },
  },
  mounted() {
    this.getCharacters();
  },
};
</script>
<template>
  <AppHeader title="Breaking Bad API App" />
  <main>
    <AppMain @startFilter="getCharacters()"/>
  </main>
</template>

<style lang="scss">
@use "./styles/general";
</style>