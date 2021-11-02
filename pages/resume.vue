<template>
  <!-- Resume Tab -->
  <section>
    <div class="resume-header">
      <h2>RESUME</h2>
      <a
        :href="`${publicPath}francescamccormickresume.pdf`"
        target="_blank"
        class="download-button"
      >Download</a>
    </div>
    <div class="resume-container">
      <div class="resume-frame">
        <img
          :src="getImgUrl(resumeImg)"
          alt="Francesca's Resume"
          class="resume-image"
        >
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data () {
    return {
      publicPath: process.env.BASE_URL,
      resumeImg: 'francescamccormickresume'
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
/* Resume Page */

.resume-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.download-button {
  text-decoration: none;
  border: 3px solid #f56200;
  height: 3.125rem;
  width: 10rem;
  background-color: #ad2a67;
  color: white;
  border-radius: 4px;
  /* margin: 0 auto; */
  display: flex;
  align-items: center;
  justify-content: center;

  &:hover {
    background-color: white;
    color: #ad2a67;
  }
}

.resume-container {
  display: flex;
  justify-content: center;
  align-items: center;
}

.resume-frame {
  background-color: #ad2a67;
  width: 80%;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 4px;
  padding: 2rem;
}

.resume-image {
  width: 100%;
  height: 70%;
}

@media screen and (max-width: 900px) {
  .resume-frame {
    width: 100%;
    padding: 0.5rem;
  }
}
</style>
