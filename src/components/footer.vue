<template>
  <footer>
    <v-layout row wrap>
      <v-flex xs12 sm6 md3>
        <h3 id="title">product</h3>
        <a href="#">
          <li>What is Telecare?</li>
        </a>
        <a href="#">
          <li>How much does Vala cost?</li>
        </a>
        <a href="#">
          <li>Mental Health</li>
        </a>
        <a href="#">
          <li>Emergency Appointments</li>
        </a>
      </v-flex>
      <v-flex xs12 sm6 md3>
        <h3 id="title">company</h3>
        <a href="#">
          <li>News & Views</li>
        </a>
        <a href="#">
          <li>Get in touch</li>
        </a>
        <a href="#">
          <li>Physician Associates</li>
        </a>
        <a href="#">
          <li>FAQs</li>
        </a>
      </v-flex>
      <v-flex xs12 sm6 md3>
        <h3 id="title">legal</h3>
        <a href="#">
          <li>Prescription policy</li>
        </a>
        <a href="#">
          <li>Registration & regulation</li>
        </a>
        <a href="#">
          <li>Privacy policy</li>
        </a>
        <a href="#">
          <li>Data protection</li>
        </a>
      </v-flex>
      <v-flex xs12 sm6 md3 class="d-flex justify-content-around">
        <v-layout row wrap>
          <a href="http://linkedin.com">
            <i class="fa fa-linkedin"></i>
          </a>

          <a href="http://facebook.com">
            <i class="fa fa-facebook-f"></i>
          </a>

          <a href="http://twitter.com">
            <i class="fa fa-twitter"></i>
          </a>
        </v-layout>
      </v-flex>
    </v-layout>
  </footer>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
footer {
  padding: 30px 40px;
  background-image: linear-gradient(#b3c6cc, #e9e9e9);
  display: flex;
  align-items: center;
  list-style: none;
  font-size: 14px;
}

#title {
  margin: 30px 0 0 20px;
  text-transform: uppercase;
}

li {
  height: 40px;
}

i {
  color: #000000;
  font-size: 2em;
}

i:hover {
  color: #0082ad;
}
</style>