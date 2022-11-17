<script>
export default {
  name: "ActorCard",
  props: {
    actor: Object,
  },
};
</script>

<template>
  <div class="mc-card col-3 m-4">
    <div class="img-area">
      <img :src="actor.img" :alt="actor.name" />
    </div>
    <div class="text-area">
      <h4>{{ actor.name }}</h4>
      <span>{{ actor.category }}</span>
      <p>{{ actor.status }}</p>
    </div>
  </div>
</template>


<style lang="scss" scoped>
.mc-card {
  background-color: #333c46;
  padding: 15px;
  text-align: center;
  img {
    object-fit: cover;
    max-width: 100%;
  }
  h4 {
    font-weight: 700;
    margin: 20px 0px;
    color: white;
  }
  span,
  p {
    text-transform: uppercase;
    color: #747171;
  }
  p {
    margin: 15px 0px;
  }
}
</style>