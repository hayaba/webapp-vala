<template>
  <footer>
    <v-layout row wrap>
      <v-flex xs12 sm6 md3>
        <li>
          <b>Product</b>
        </li>
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
        <li>
          <b>Company</b>
        </li>
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
        <li>
          <b>Legal</b>
        </li>
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

li {
  height: 40px;
}

i {
  color: #0082ad;
  font-size: 2em;
  margin-left: 30px;
}
</style>