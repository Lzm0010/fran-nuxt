<template>
  <!-- Resume Tab -->
  <section>
    <h2>REVIEWS</h2>
    <div class="reviews-container">
      <div class="reviews-frame">
        <div class="reviews">
          <div class="review">
            <div class="header-row">
              <h4>That's Enough Now Thanks</h4>
            </div>
            <p>
              “I have been writing and directing short films for eight years.
              I have worked with professional actors in both New Mexico and California.
              I recently finished shooting That’s Enough Now Thanks and had the pleasure of
              working with Francesca Barker McCormick as our secondary lead.
            </p>
            <p>
              During photography I quickly noticed Francesca had a well honed tool kit of
              technical skills along with an innate acting ability. She came well prepared for
              each scene, with a clear grasp of tone and substance. I was imminently
              impressed. Her performance on-screen is engaging and energized, and remains
              consistently terrific even at the end of a long day of shooting.
              She was a joy to work with, meeting our small production with enthusiasm and
              creativity. Her on set presence is calm, collected and dedicated. I highly
              recommend you consider casting Francesca in any upcoming projects!"
            </p>
            <p class="reviewer">
              - Aquila Chase-Daniel
            </p>
          </div>
          <div class="review">
            <div class="header-row">
              <h4>Skylife - Ashley</h4>
              <!-- <img
                class="review-image"
                :src="getPng('skylife')"
                alt="Skylife"
              > -->
            </div>
            <p>
              “You think it is a given but the fact that Francesca knew her
              lines inside and out, where I was not distracted by an actor
              searching for his/her lines or stumbling over words… I was
              simply focused on the performance and thinking to myself ‘this
              actress captures the essence of the character’s
              eloquence/frustration and emotional bandwidth’. I kept
              watching the screen for any signs of dishonesty in the
              performance but I could find none. An actor gets a few seconds
              or a few minutes to showcase his/her ability to
              deliver…preparation /performance dictates the former or the
              latter.
            </p>
            <p>
              As a writer who spends an enormous amount of time developing
              characters and their stories, I work very hard building the
              ideal cast. It takes me more time than most to find the ideal
              talent only because I know my characters so well and the world
              in which they live. What I see and hear in my head is not
              always easy to match beyond my imagination. You want talent
              that can deliver. Talent who will put in the work. Not
              everyone is willing to do that.
            </p>
            <p>
              I am extremely satisfied and pleased with the cast assembled
              for SKYLIFE - ‘Heroes and Heroines’ (proof of concept). When
              an actor is right for a role, when research and rehearsals are
              fully explored… it makes for a much smoother production and
              authentic performance.
            </p>
            <p>
              It was evident Francesca understood the essence of Ashley, her
              inner and outer struggles… Francesca made it effortless. It
              was a pleasure to watch Francesca bring this character to
              life. ”
            </p>
            <p class="reviewer">
              - Marvalee Peart
            </p>
          </div>
          <div class="review">
            <div class="header-row">
              <h4>How to Find Love In A Pandemic - Summer</h4>
              <!-- <img
                class="review-image"
                :src="getPng('howtofindlove')"
                alt="How to Find Love in a Pandemic"
              > -->
            </div>
            <p>
              “Francesca is a joy to work with! Her eagerness to dive into
              the work, the character development she brought to the role,
              and her comedic timing all stood out to us. She took what we
              wrote and brought her own unique choices to Summer to create a
              hilarious and full character. On top of that, she is a warm,
              kind, and supportive supportive presence in any room. We can’t
              wait to work with her again!”
            </p>
            <p class="reviewer">
              - Joe Bridgewood & Emily Blake Anderson
            </p>
          </div>
          <div class="review">
            <h4>SinFull - Dr. Alicia Serrano</h4>
            <p>
              “Watching Francesca bring Dr. Alicia to life was such a
              powerfully beautiful moment to witness as a writer. She
              painted her in ways that I hadn't even imagined and brought
              such a riveting sense of compassion and heartbreak to the
              role. I think the audience will be quite taken by her ability
              to ground you, the viewer, into the intimacy of Alicia's inner
              turmoil. ”
            </p>
            <p class="reviewer">
              - Asha Etchison
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
// export default {
//   methods: {
//     getPng (img) {
//       const images = require.context('assets/images', false, /\.png$/)
//       return images('./' + img + '.png')
//     }
//   }
// }
</script>

<style lang="scss" scoped>
/* Reviews Page */

.reviews-container {
  display: flex;
  justify-content: center;
  align-items: center;
}

.reviews-frame {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 2rem;
  background-color: #2e3138;
  border-radius: 4px;
  width: 80%;
}

.reviews {
  background-color: white;
  display: flex;
  flex-direction: column;
  border-radius: 4px;
  padding: 3rem;

  .review {
    display: flex;
    flex-direction: column;
    align-items: flex-start;

    h4 {
      color: #ad2a67;
    }

    .review-image {
      height: 30%;
      width: 30%;
    }

    .reviewer {
      color: #f56200;
    }
  }
}

@media screen and (max-width: 900px) {
  .review-image {
    flex-basis: 95%;
  }
}
</style>
