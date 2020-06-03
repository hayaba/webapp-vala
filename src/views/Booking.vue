<template>
  <div>
    <v-row id="title-box">
      <v-flex>
        <h1 id="first-title">
          Affordable, private
          online mental health support
        </h1>
        <br />
        <br />
        <h2 id="second-title">Talk with a qualified medical professional today</h2>
      </v-flex>
    </v-row>
    <v-layout row wrap id="booking-card">
      <v-flex xs12 sm6 md4>
        <v-col md8>
          <v-card id="join-vala">
            <h4>Join Vala</h4>
            <v-card-text>
              <h4 id="descreption">
                Welcome to Vala, for all your health and wellbeing needs. We look forward to being
                with you when you need us.
              </h4>
              <br />
              <span>Vala is available to UK Residents (at home or abroad) and visitors to the UK.</span>
            </v-card-text>
            <v-row id="booking-btn">
              <router-link to="/Booking">
                <v-btn id="booking1">Booking</v-btn>
              </router-link>
            </v-row>
          </v-card>
        </v-col>
      </v-flex>

      <v-flex d-flex xs12 sm6 md4>
        <v-col md8>
          <v-card>
            <v-card-text>
              <b>If you are not ready, please do stay in touch.</b>
            </v-card-text>

            <v-form v-model="valid">
              <v-text-field v-model="name" :rules="nameRules" label="Name" required></v-text-field>
              <v-text-field v-model="email" :rules="emailRules" label="E-mail" required></v-text-field>
              <v-row id="booking-btn">
                <v-btn @click="submit" id="submit">stay in touch</v-btn>
              </v-row>
            </v-form>
          </v-card>
        </v-col>
      </v-flex>
    </v-layout>

    <v-layout row wrap id="review">
      <v-flex xs1 md1>
        <div class="border-bubble"></div>
      </v-flex>
      <v-flex xs11 md2>
        <div class="review-text">
          <a href="https://uk.trustpilot.com/review/www.valahealth.com" id="title-link">
            Vala health - highly
            <br />recommend
            <br />
          </a>
          <br />
          <p>
            Felt really reassured that I was getting trustworthy advice,
            being properly listened to and was super friendly as well
          </p>
          <a href="https://uk.trustpilot.com/review/www.valahealth.com">
            <v-img src="@/assets/truspilot.png" width="86px"></v-img>
          </a>
        </div>
      </v-flex>

      <v-flex xs12 md4>
        <v-img
          src="https://firebasestorage.googleapis.com/v0/b/webapp-vala.appspot.com/o/illust3.png?alt=media&token=7ac55f47-4c74-4df6-9a9e-807ae3e275a1"
        ></v-img>
      </v-flex>
    </v-layout>
  </div>
</template>

<script>
export default {
  data: () => ({
    valid: false,
    name: "",
    nameRules: [v => !!v || "Name is required"],
    email: "",
    emailRules: [
      v => !!v || "E-mail is required",
      v =>
        /^\w+([.-]?\w+)*@\w+([.-]?\w+)*(\.\w{2,3})+$/.test(v) ||
        "E-mail must be valid"
    ]
  })
};
</script>

<style lang="scss" scoped>
#title-box {
  background-color: #0082ad;
  height: 244px;
  text-align: center;
}

#first-title {
  margin-top: 60px;
  color: #f5f5f5;
  font-weight: normal;
}

#second-title {
  color: #f5f5f5;
  font-weight: normal;
}

#booking-card {
  justify-content: center;
  margin-top: 80px;
  text-align: center;
}

#booking1 {
  background-color: #e6d698;
}

#descreption {
  line-height: 34px;
}

#join-vala {
  padding-top: 20px;
}

.v-card {
  background-color: #b3c6cc;
}

.v-form {
  padding: 0 20px 0 20px;
}

#submit {
  background-color: #e6d698;
}

#review {
  display: flex;
  align-items: center;
  justify-content: center;
}

a {
  color: #f5f5f5;
}

#title-link:hover {
  text-decoration: underline solid;
}

.review-text {
  margin-top: 20px;
  padding: 20px;
  position: relative;
  color: #f5f5f5;
  background: #0082ad;
  border-radius: 0.7em;
}

.review-text:after {
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
  height: 240px;
  width: 320px;
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
</style>