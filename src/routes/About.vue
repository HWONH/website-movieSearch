<template>
  <div class="about">
    <div class="photo">
      <img
        src="~/assets/logo.png"
        :alt="name" /> <!-- :src="image" -->
    </div>
    <div class="name">
      {{name}}
    </div>
    <div>{{email}}</div>
    <div>{{blog}}</div>
    <div>{{phone}}</div>
  </div>
</template>

<script>
export default {
  computed: {
    image() {
      return this.$store.state.about.image
    },
    name() {
      return this.$store.state.about.name
    },
    email() {
      return this.$store.state.about.email
    },
    blog() {
      return this.$store.state.about.blog
    },
    phone() {
      return this.$store.state.about.phone
    }
  }
}
</script>

<style lang="scss" scoped>
@import "~/scss/main";
.about {
  text-align: center;
  .photo {
    width: 250px;
    height: 250px;
    margin: 40px auto 20px;
    padding: 30px;
    border: 10px solid $gray-300;
    border-radius: 50%;
    box-sizing: border-box;
    background-color: $gray-200;
    img {
      width: 100%;
    }
  }
  .name {
    margin-bottom: 20px;
    font-family: "Oswald", sans-serif;
    font-size: 40px;
  }
}
</style>