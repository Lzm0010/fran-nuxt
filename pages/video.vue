<template>
  <!-- Video Tab -->
  <section>
    <h2>VIDEO</h2>
    <div class="video-container">
      <h4 class="video-title">
        SELF TAPE REEL
      </h4>
      <div class="video-frame">
        <iframe
          class="video-iframe"
          src="https://www.youtube.com/embed/IlNpaV5WW6g"
          frameborder="0"
          allowfullscreen
        />
      </div>
      <h4 class="video-title">
        PROJECT REEL
      </h4>
      <div class="video-frame">
        <iframe
          class="video-iframe"
          src="https://www.youtube.com/embed/sUuQZBhp_TM"
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
  background-color: #ad2a67;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 4px;
  padding: 2rem;
  margin: 0.5rem;
}

.video-iframe {
  height: 43rem;
  width: 50rem;
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
