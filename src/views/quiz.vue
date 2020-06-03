<template>
  <div id="questions">
    <h3 id="statment">
      This quiz doesn’t substitute professional medical assessment,
      and it’s purpose only to give you some insights
      <br />to common
      features in mental health and it may or may not reflect your true individual case.
    </h3>

    <p v-if="scored == null">Start the quiz here:</p>

    <h4>1. In the last two weeks, feeling less interested in meeting friends or doing activities:</h4>
    <input type="radio" value="4" v-model="questions.qustion1" />
    <label for="one">Not at all</label>
    <br />
    <input type="radio" value="3" v-model="questions.qustion1" />
    <label for="two">Some days</label>
    <br />
    <input type="radio" value="2" v-model="questions.qustion1" />
    <label for="two">Most of the days</label>
    <br />
    <input type="radio" value="1" v-model="questions.qustion1" />
    <label for="two">Almost everyday</label>
    <br />
    <br />

    <h4>2. Feeling low in energy when doing daily activities:</h4>
    <input type="radio" value="4" v-model="questions.qustion2" />
    <label for="one">Not at all</label>
    <br />
    <input type="radio" value="3" v-model="questions.qustion2" />
    <label for="two">Some days</label>
    <br />
    <input type="radio" value="2" v-model="questions.qustion2" />
    <label for="two">Most of the days</label>
    <br />
    <input type="radio" value="1" v-model="questions.qustion2" />
    <label for="two">Almost everyday</label>
    <br />
    <br />

    <h4>3. Lack of sleep, sleeping restlessly, or oversleeping:</h4>
    <input type="radio" value="4" v-model="questions.qustion3" />
    <label for="one">Not at all</label>
    <br />
    <input type="radio" value="3" v-model="questions.qustion3" />
    <label for="two">Some days</label>
    <br />
    <input type="radio" value="2" v-model="questions.qustion3" />
    <label for="two">Most of the days</label>
    <br />
    <input type="radio" value="1" v-model="questions.qustion3" />
    <label for="two">Almost everyday</label>
    <br />
    <br />

    <h4>4. Reduced or increased appetite:</h4>
    <input type="radio" value="4" v-model="questions.qustion4" />
    <label for="one">Not at all</label>
    <br />
    <input type="radio" value="3" v-model="questions.qustion4" />
    <label for="two">Some days</label>
    <br />
    <input type="radio" value="2" v-model="questions.qustion4" />
    <label for="two">Most of the days</label>
    <br />
    <input type="radio" value="1" v-model="questions.qustion4" />
    <label for="two">Almost everyday</label>
    <br />
    <br />

    <h4>5. Hard to focus while doing fairly usual mental tasks:</h4>
    <input type="radio" value="4" v-model="questions.qustion5" />
    <label for="one">Not at all</label>
    <br />
    <input type="radio" value="3" v-model="questions.qustion5" />
    <label for="two">Some days</label>
    <br />
    <input type="radio" value="2" v-model="questions.qustion5" />
    <label for="two">Most of the days</label>
    <br />
    <input type="radio" value="1" v-model="questions.qustion5" />
    <label for="two">Almost everyday</label>
    <br />
    <br />

    <h4>6. Feeling worried about the future and/or thinking too much about the past:</h4>
    <input type="radio" value="4" v-model="questions.qustion6" />
    <label for="one">Not at all</label>
    <br />
    <input type="radio" value="3" v-model="questions.qustion6" />
    <label for="two">Some days</label>
    <br />
    <input type="radio" value="2" v-model="questions.qustion6" />
    <label for="two">Most of the days</label>
    <br />
    <input type="radio" value="1" v-model="questions.qustion6" />
    <label for="two">Almost everyday</label>
    <br />
    <br />

    <h4>7. Feeling guilty or low self-worth:</h4>
    <input type="radio" value="4" v-model="questions.qustion7" />
    <label for="one">Not at all</label>
    <br />
    <input type="radio" value="3" v-model="questions.qustion7" />
    <label for="two">Some days</label>
    <br />
    <input type="radio" value="2" v-model="questions.qustion7" />
    <label for="two">Most of the days</label>
    <br />
    <input type="radio" value="1" v-model="questions.qustion7" />
    <label for="two">Almost everyday</label>
    <br />
    <br />

    <h4>8. Feeling down, depressed or hopeless:</h4>
    <input type="radio" value="4" v-model="questions.qustion8" />
    <label for="one">Not at all</label>
    <br />
    <input type="radio" value="3" v-model="questions.qustion8" />
    <label for="two">Some days</label>
    <br />
    <input type="radio" value="2" v-model="questions.qustion8" />
    <label for="two">Most of the days</label>
    <br />
    <input type="radio" value="1" v-model="questions.qustion8" />
    <label for="two">Almost everyday</label>
    <br />
    <br />

    <h4>9. Having uncontrollable negative thoughts:</h4>
    <input type="radio" value="4" v-model="questions.qustion9" />
    <label for="one">Not at all</label>
    <br />
    <input type="radio" value="3" v-model="questions.qustion9" />
    <label for="two">Some days</label>
    <br />
    <input type="radio" value="2" v-model="questions.qustion9" />
    <label for="two">Most of the days</label>
    <br />
    <input type="radio" value="1" v-model="questions.qustion9" />
    <label for="two">Almost everyday</label>

    <br />
    <br />
    <span v-if="quizComplete">Your score is {{ scored }} out of 36</span>
    <v-col cols="8" id="result">
      <p v-if="quizComplete">Thanks for taking time to complete the questions.</p>
      <p v-if="scored >= 1 && scored < 18">
        While you might be feeling down right now, you’re not showing signs of depression.
        Those low feelings should go away
        as the problem passes but you can help things along by trying some of the ideas below
      </p>
      <p v-if="scored >= 18">
        If you’re having thoughts most days about hurting or
        killing yourself please reach out straight away and talk to someone who’s trained to help.
        Even if you feel like no-one in the world gets you right now, there are people who can support you.
        These thoughts are common in depression but find they are getting more frequent
        (most days) or you feel more like acting on them - call us straight away.
      </p>
    </v-col>
  </div>
</template>


<script>
/* eslint-disable */
export default {
  data() {
    return {
      quizComplete: false,
      questions: {
        qustion1: null,
        qustion2: null,
        qustion3: null,
        qustion4: null,
        qustion5: null,
        qustion6: null,
        qustion7: null,
        qustion8: null,
        qustion9: null
      }
    };
  },

  watch: {},
  computed: {
    scored() {
      var q1 = Number(this.questions.qustion1);
      var q2 = Number(this.questions.qustion2);
      var q3 = Number(this.questions.qustion3);
      var q4 = Number(this.questions.qustion4);
      var q5 = Number(this.questions.qustion5);
      var q6 = Number(this.questions.qustion6);
      var q7 = Number(this.questions.qustion7);
      var q8 = Number(this.questions.qustion8);
      var q9 = Number(this.questions.qustion9);
      if (q9 == 1 || q9 == 2 || q9 == 3 || q9 == 4) {
        this.quizComplete = true;
        return q1 + q2 + q3 + q4 + q5 + q6 + q7 + q8 + q9;
      }
    }
  }
};
</script>

<style lang="scss" scoped>
#statment {
  color: rgb(219, 2, 2);
  margin-bottom: 20px;
  line-height: 30px;
}

#questions {
  background-image: linear-gradient(#b3c6cc, #e9e9e9, #e9e9e9);
  padding: 60px;
  line-height: 30px;
}

#result {
  padding: 12px 0;
}
</style>