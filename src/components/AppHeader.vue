<script>
export default {
  name: "AppHeader",
  props: {
    title: String,
  },
};
</script>

<template>
  <header>
    <div class="container d-flex align-items-center">
      <div class="logo">
        <img src="/Breaking_Bad_logo.svg" alt="" />
      </div>
      <h1>{{ title }}</h1>
    </div>
  </header>
</template>


<style lang="scss" scoped>
header {
  padding: 20px;
}
.logo {
  width: 130px;
}
img {
  width: 100%;
  vertical-align: middle;
}
h1 {
  color: white;
  font-weight: 700;
  margin-left: 50px;
}
</style>