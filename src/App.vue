<script>
import axios from "axios";
import store from "./data/store";

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
      axios
        .get(store.apiUrlBrBa)
        .then((result) => {
          console.log(result.data);
        })
        .catch((error) => {
          console.log(error);
        });
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
    <AppMain />
  </main>
</template>

<style lang="scss">
@use "./styles/general";
</style>