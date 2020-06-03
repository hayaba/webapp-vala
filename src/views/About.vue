<template>
  <div class="about">
    <h1>About Vala</h1>

    <v-layout row wrap id="review-section">
      <v-flex xs1 md1>
        <div class="border-bubble"></div>
      </v-flex>
      <v-flex xs11 md3>
        <div class="review-bubble">
          <a href="https://uk.trustpilot.com/review/www.valahealth.com">I had a wonderful experience</a>
          <p>
            <br />Brilliant. Really convenient and easy to you. I had a worry I wanted to address (difficult in these lock down times) and as someone with anxiety having to wait weeks for an appointment is very tough. This was a breath of fresh air.
          </p>
          <a href="https://uk.trustpilot.com/review/www.valahealth.com">
            <v-img src="@/assets/truspilot.png" width="86px"></v-img>
          </a>
        </div>
      </v-flex>

      <v-flex xs12 md6>
        <v-img
          src="https://firebasestorage.googleapis.com/v0/b/webapp-vala.appspot.com/o/illust1.png?alt=media&token=326d7892-eddb-45af-8c9d-5b7cb0531b33"
        ></v-img>
      </v-flex>
    </v-layout>

    <v-layout row wrap id="description">
      <v-flex xs12 md12>
        <h1 id="title">#HealthMatters</h1>
      </v-flex>
      <v-flex>
        <p>
          Vala is a video consulting service that enables people to have health and social care appointments
          from home or wherever
          <br />is convenient.
          All you need is a device for making video calls like a
          smartphone and an internet connection.
          <br />Vala is a secure form of video consulting approved for use by
          the Care Quality Commission.
        </p>
      </v-flex>
    </v-layout>

    <div class="container">
      <v-row>
        <v-col cols="8" sm="6">
          <v-layout row wrap>
            <v-avatar size="70">
              <img src="../assets/profile-1.jpg" alt="Dr. Niall Aye-Maung" />
            </v-avatar>

            <div class="text-center">
              <h3>Dr. Niall Aye-Maung</h3>
              <p>
                General Practitioner, Co-Founder
                <br />and Chief Medical Officer
              </p>
            </div>
          </v-layout>
        </v-col>
        <v-col cols="4" sm="5">
          <v-layout row wrap>
            <v-avatar size="70">
              <img src="../assets/profile-3.jpg" alt="Dr. Niall Aye-Maung" />
            </v-avatar>

            <div class="text-center">
              <h3>Shellane Crisotomo</h3>
              <p>
                Physician Associate,
                <br />Co-Founder
              </p>
            </div>
          </v-layout>
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="8" sm="6">
          <v-layout row wrap>
            <v-avatar size="70">
              <img src="../assets/profile-7.jpg" alt="Dr. Niall Aye-Maung" />
            </v-avatar>

            <div class="text-center">
              <h3>Pete Trainor</h3>
              <p>Chief Executive Officer (CEO)</p>
            </div>
          </v-layout>
        </v-col>
        <v-col cols="4" sm="5">
          <v-layout row wrap>
            <v-avatar size="70" class="padding-left-300">
              <img src="../assets/profile-8.jpg" alt="Dr. Niall Aye-Maung" />
            </v-avatar>
            <div class="text-center">
              <h3>Marta Villar</h3>
              <p>Finance Director</p>
            </div>
          </v-layout>
        </v-col>
      </v-row>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
h1 {
  text-align: center;
  margin: 40px 0;
}

#review-section {
  display: flex;
  align-items: center;
  justify-content: center;
}

a {
  color: #f5f5f5;
}

a:hover {
  text-decoration: underline solid;
}

.review-bubble {
  margin-top: 20px;
  padding: 20px;
  position: relative;
  color: #f5f5f5;
  background: #0082ad;
  border-radius: 0.7em;
}

.review-bubble:after {
  content: "";
  position: absolute;
  right: 0;
  top: 50%;
  width: 0;
  height: 0;
  border: 30px solid transparent;
  border-left-color: #0082ad;
  border-right: 0;
  border-bottom: 0;
  margin-top: -70px;
  margin-right: -30px;
}

.border-bubble {
  position: relative;
  border: solid #81b3aa;
  color: #f5f5f5;
  border-radius: 1em;
  height: 300px;
  width: 440px;
}

.border-bubble:before {
  content: "";
  position: absolute;
  left: 0;
  top: 40%;
  width: 0;
  height: 0;
  border: 31px solid transparent;
  border-right-color: #81b3aa;
  border-left: 0;
  border-bottom: 0;
  // margin-top: -10.5px;
  margin-left: -31px;
}

.border-bubble:after {
  content: "";
  position: absolute;
  left: 0;
  top: 40%;
  width: 0;
  height: 0;
  border: 24px solid transparent;
  border-right-color: #f5f5f5;
  border-left: 0;
  border-bottom: 0;
  margin-top: 3px;
  margin-left: -24px;
}

#description {
  background-image: linear-gradient(#0082ad, #b3c6cc);
  text-align: center;
}

#title {
  color: #e6d698;
  letter-spacing: 0.05em;
  text-transform: capitalize;
}

.container {
  height: auto;
}

.v-avatar {
  margin: 20px;
}

.text-center {
  margin-top: 30px;
}
</style>
