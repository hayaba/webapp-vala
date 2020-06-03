<template>
  <div class="home">
    <v-img src="@/assets/finalposter.png"></v-img>

    <v-row grid-list-md text-xs>
      <v-flex id="steps-title">
        <h2>
          Ready to speak to Vala?
          <br />
        </h2>
      </v-flex>
    </v-row>

    <v-layout row wrap id="container">
      <v-flex xs12 md3>
        <v-list-item class="justify-items-center">
          <v-list-item-content>
            <v-list-item-title class="headline">1. PICK A TIME</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <img id="icon1" class="icon" src="@/assets/st1.svg" alt />
        <v-card-text>
          Pick a time that suites
          your schedule
        </v-card-text>
      </v-flex>
      <v-flex xs12 md3>
        <v-list-item>
          <v-list-item-content>
            <v-list-item-title class="headline">2. BOOK</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <img id="icon2" class="icon" src="@/assets/st2.svg" alt />
        <v-card-text>Book an appointment</v-card-text>
      </v-flex>
      <v-flex xs12 md3>
        <v-list-item>
          <v-list-item-content>
            <v-list-item-title class="headline">3. CALL</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <img id="icon3" class="icon" src="@/assets/st3.svg" alt />
        <v-card-text>Talk to a specialist over video/phone</v-card-text>
      </v-flex>
      <v-flex xs12 md3>
        <v-list-item>
          <v-list-item-content>
            <v-list-item-title class="headline">4. FOLLOW UP</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <img id="icon4" class="icon" src="@/assets/st4copy.svg" alt />
        <v-card-text>
          Agree on follow/up and
          support plan that works
          for you
        </v-card-text>
      </v-flex>
    </v-layout>

    <v-row id="booking-btn">
      <router-link to="/Booking">
        <v-btn id="booking">Booking</v-btn>
      </router-link>
    </v-row>

    <v-layout row wrap id="video-section">
      <v-flex xs12 id="video-title" tag="h2">What is telemedicine?</v-flex>
      <v-flex xs12 id="video-text" tag="p">
        The coronavirus pandemic has overwhelmed hospitals, physicians and the medical community.
        <br />That’s pushed telemedicine into the hands of providers and patients as the first response for
        <br />primary care. Telemedicine isn’t new to the medical community, and here’s how it works:
      </v-flex>
      <v-flex xs12 id="video">
        <iframe
          width="500"
          height="260"
          src="https://www.youtube.com/embed/yl2VPqZPC7k"
          frameborder="0"
          allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen
        ></iframe>
      </v-flex>
    </v-layout>

    <v-layout row wrap>
      <v-flex xs12 md6>
        <v-img
          src="https://firebasestorage.googleapis.com/v0/b/webapp-vala.appspot.com/o/ill2.png?alt=media&token=befd2898-0ddb-48d9-9bf3-2716176341c3"
        ></v-img>
      </v-flex>
      <v-flex xs12 md4 id="quiz-section">
        <div class="speech-bubble">
          <h3 id="text-quiz">Are you not sure about calling us yet?</h3>
          <br />
          <p>
            Feelings and emotions are part of our humanity,
            but sometimes it is difficult to define them. Feeling
            down for a long time can be a sign to seek help.
          </p>
          <p>
            You can take this quick self-assessment to help
            you understand better how you’ve been feeling in
            the last two weeks.
          </p>

          <router-link to="/quiz">
            <v-btn id="quiz-btn">start quiz</v-btn>
          </router-link>
        </div>
      </v-flex>
    </v-layout>
  </div>
</template>

<script>
import { TweenMax, Power2 } from "gsap";
export default {
  name: "Home",
  mounted() {
    const icons = document.querySelectorAll(".icon");

    TweenMax.staggerTo(icons, 1, {
      filter: "grayscale(0)",
      "-webkit-filter": "grayscale(0)",
      scale: 1.5,
      ease: Power2.easeIn,

      stagger: {
        each: 4,
        yoyo: true
      },
      repeat: -1,
      repeatDelay: 2
    });
  }
};
</script>

<style>
.row {
  justify-content: center;
}

#steps-title {
  text-align: center;
  margin: 60px 0;
}

#container {
  margin: 0;
  display: flex;
  align-items: center;
  text-align: center;
}

.icon {
  display: flex;
  filter: grayscale(100%);
  justify-items: center;
  width: 180px;
  height: 200px;
  margin: 80px;
}

#booking-btn {
  height: 200px;
  justify-content: center;
  align-content: center;
}

#booking {
  background-color: #e6d698;
  height: 60px;
  width: 140px;
}

#video-title {
  height: 60px;
}

#text-quiz {
  color: #e6d698;
}

p {
  line-height: 170%;
  margin-bottom: 20px;
}

#video {
  margin: 60px 0;
}

#video-section {
  background-image: linear-gradient(#f5f5f5, #81b3aa, #0082ad 80%);
  width: 100vw;
  text-align: center;
}

#quiz-btn {
  background-color: #e6d698;
  display: flex;
}

.speech-bubble {
  padding: 20px;
  position: relative;
  background: #0082ad;
  color: #f5f5f5;
  border-radius: 0.7em;
}

.speech-bubble:after {
  content: "";
  position: absolute;
  left: 0;
  top: 40%;
  width: 0;
  height: 0;
  border: 31px solid transparent;
  border-right-color: #0082ad;
  border-left: 0;
  border-bottom: 0;
  margin-top: -40.5px;
  margin-left: -31px;
}

#quiz-section {
  display: flex;
  align-items: center;
  margin: 4px;
}
</style>