<script>
export default {
  name: "AppHeader",
};
</script>

<template>
  <header>
    <div class="container d-flex align-items-center">
      <div class="logo">
        <img src="/public/Breaking_Bad_logo.svg" alt="" />
      </div>
      <h1>Breaking Bad API Cast</h1>
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
  margin-left: 50px;
}
</style>