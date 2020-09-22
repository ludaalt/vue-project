<template>
<div class="container">
    <form>
            <InputLabel :fields="fields"/>
            <ButtonRectangle class="blue-button" :msg="msg"/>
    </form>
</div>
</template>

<script>
import InputLabel from '@/components/InputLabel.vue';
import ButtonRectangle from '@/components/ButtonRectangle.vue';

export default {
  data() {
    return {
      fields: [
        {
          label: 'Email',
          placeholder: 'example@acme.com',
          inputName: 'email',
        },
        {
          label: 'Password',
          placeholder: '••••••••',
          inputName: 'pass',
        },
      ],
      msg: 'Sign In',
    };
  },

  components: {
    InputLabel, ButtonRectangle,
  },
};
</script>

<style>
.container {
    margin: 0 auto;
}
form {
    margin: 0 auto;
    max-width: 300px;
    background: #FFFFFF;
    border-radius: 40px;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.blue-button button {
  background-color: #1E1A3E;
  color: #FFFFFF;
  padding-left: 50px;
  padding-right: 50px;
  margin-top: 40px;
  margin-bottom: 20px;
}
</style>
