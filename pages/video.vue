<template>
  <!-- Video Tab -->
  <section>
    <h2>VIDEO</h2>
    <div class="video-container">
      <h4 class="video-title">
        2022 REEL
      </h4>
      <div class="video-frame">
        <iframe
          class="video-iframe"
          src="https://www.youtube.com/embed/y71bbi516xg"
          frameborder="0"
          allowfullscreen
        />
      </div>
    </div>
  </section>
</template>

<script>
</script>

<style lang="scss" scoped>
/* Video Page */

.video-container {
  margin-top: -6rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.video-title {
  font-size: 2.5rem;
  font-family: "crushed", Arial, Helvetica, sans-serif;
}

.video-frame {
  background-color: #2e3138;;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 4px;
  padding: 1rem;
  margin: 0.5rem;
}

.video-iframe {
  height: 27rem;
  width: 48rem;
}

@media screen and (max-width: 900px) {
  .video-frame {
    width: 90%;
    padding: 0.5rem;
  }

  .video-iframe {
    height: 100%;
    width: 100%;
  }
}
</style>
