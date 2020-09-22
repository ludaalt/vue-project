<template>
  <div>
      <h1>Ready for a great User experience?</h1>
      <p class="home-text">Bring your media to the next level!</p>
      <p class="buttons-container">
        <router-link to="/signup"><ButtonRectangle :msg="msg"/></router-link>
        <router-link to="/signup"><ButtonRound /></router-link>
      </p>
      <p><img alt="Woman" src="../assets/woman1.jpg"></p>
  </div>
</template>

<script>
import ButtonRound from '@/components/ButtonRound.vue';
import ButtonRectangle from '@/components/ButtonRectangle.vue';

export default {
  data() {
    return {
      msg: 'Sign Up',
    };
  },
  components: {
    ButtonRound, ButtonRectangle,
  },
};
</script>

<style>
.home-text {
  font-weight: normal;
  font-size: 14px;
  line-height: 20px;
  text-align: center;
  letter-spacing: 0.02em;
  color: #3E4462;
}

.buttons-container {
  max-width: 200px;
  margin: 0 auto;
  display: flex;
  justify-content: space-evenly;
  margin-top: 30px;
  margin-bottom: 30px;
}
</style>
