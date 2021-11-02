<template>
  <div>
    <!-- Photos Tab -->
    <section>
      <h2>PHOTOS</h2>
      <div class="headshots">
        <img
          v-for="(headshot, index) in headshots"
          :key="index"
          class="headshot"
          :src="getImgUrl(headshot)"
          :alt="`Francesca Headshot ${index}`"
        >
      </div>
    </section>
  </div>
</template>

<script>
export default {
  data () {
    return {
      headshots: ['fran0', 'fran1', 'fran2', 'fran3', 'fran4', 'fran5', 'fran6', 'fran7']
    }
  },
  methods: {
    getImgUrl (img) {
      const images = require.context('assets/images', false, /\.jpg$/)
      return images('./' + img + '.jpg')
    }
  }
}
</script>

<style lang="scss" scoped>
/* Photos Page */

.headshots {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
  align-items: flex-start;
}

.headshot {
  padding-bottom: 0.5rem;
  width: 21rem;
}
</style>
