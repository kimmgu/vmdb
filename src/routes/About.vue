<template>
  <div class="about">
    <div class="photo">
      <Loader v-if="imageLoading" absolute />
      <img :src="image" :alt="name" />
    </div>
    <div class="name">{{ name }}</div>
    <div>{{ email }}</div>
  </div>
</template>

<script>
import { mapState } from 'vuex'
import Loader from '~/components/Loader.vue'

export default {
  components: {
    Loader,
  },
  data() {
    return {
      imageLoading: true,
    }
  },
  computed: {
    ...mapState('about', ['image', 'name', 'email']),
  },
  mounted() {
    this.init()
  },
  methods: {
    async init() {
      await this.$loadImage(this.image)
      this.imageLoading = false
    },
  },
}
</script>

<style lang="scss" scoped>
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
    overflow: hidden;
    position: relative;
    img {
      height: 100%;
      position: absolute;
      top: 0;
      left: 0;
    }
  }
  .name {
    font-size: 32px;
    font-family: 'Oswald', sans-serif;
    margin-bottom: 20px;
  }
}
</style>
