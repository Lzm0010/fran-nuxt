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
      <h4 class="photo-title">
        PROJECT PHOTOS
      </h4>
      <h5 class="photo-subtitle">
        SKYLIFE PHOTOS
      </h5>
      <div class="headshots">
        <img
          v-for="(img, index) in skylifeImages"
          :key="index"
          class="skylife-photo"
          :src="getImgUrl(img)"
        >
      </div>
      <!-- <h5 class="photo-subtitle">
        SINFULL PHOTOS
      </h5>
      <div class="headshots">
        <img
          v-for="(img, index) in sinfullImages"
          :key="index"
          class="sinfull-photo"
          :src="getImgUrl(img)"
        >
      </div> -->
    </section>
  </div>
</template>

<script>
export default {
  data () {
    return {
      headshots: ['fran0', 'fran1', 'fran2', 'fran3', 'fran4', 'fran5', 'fran6', 'fran7'],
      skylifeImages: ['skylife0', 'skylife1', 'skylife2', 'skylife3'],
      sinfullImages: ['sinfull0', 'sinfull1', 'sinfull2']
      // pngImages: ['htflp0', 'htflp1']
    }
  },
  methods: {
    getImgUrl (img) {
      const images = require.context('assets/images', false, /\.jpg$/)
      return images('./' + img + '.jpg')
    },
    getPng (img) {
      const images = require.context('assets/images', false, /\.png$/)
      return images('./' + img + '.png')
    }
  }
}
</script>

<style lang="scss" scoped>
/* Photos Page */

.photo-title {
  font-size: 2.5rem;
  font-family: "crushed", Arial, Helvetica, sans-serif;
}

.photo-subtitle {
  font-size: 1.2rem;
  font-family: "crushed", Arial, Helvetica, sans-serif;
}

.headshots {
  display: flex;
  flex-wrap: wrap;
  align-items: flex-start;
  margin-bottom: 4rem;
  border: 0.5rem solid #ad2a67;
}

.headshot {
  width: 16.09rem;
}

.skylife-photo {
  width: 32.18rem;
}

.sinfull-photo {
  width: 21.45rem;
}

@media screen and (max-width: 900px) {
  .headshots{
    justify-content: space-evenly;
    border: none;
  }

  .headshot {
    width: 21rem;
    padding-bottom: 0.4rem;
  }

  .skylife-photo {
    width: 21rem;
    padding-bottom: 0.4rem;
  }

  .sinfull-photo {
    width: 21rem;
    padding-bottom: 0.4rem;
  }
}
</style>
