<template>
<div class="container">
    <form @submit="checkForm" action="#" method="post">
            <Input class="input" :fields="fields"/>
            <p v-show="isHintVisible" class="hint-text">{{ hintText }}
            </p>
            <button type="button" class="hint"
            v-on:click="isHintVisible=!isHintVisible"
            >
            </button>
            <button class="passbutton" type="button"
            @click="isPasswordVisible = !isPasswordVisible">
            </button>
            <button class="passbutton repeatPassbutton"
            type="button"
            @click="isPasswordVisible = !isPasswordVisible">
            </button>
            <ButtonRectangle class="blue-button" :msg="msg"/>
    </form>
</div>
</template>

<script>
import Input from './Input.vue';
import ButtonRectangle from './ButtonRectangle.vue';

export default {
  data() {
    return {
      fields: [
        {
          label: 'Full name',
          placeholder: 'John Doe',
          inputName: 'name',
          type: 'text',
          vModel: '',
        },
        {
          label: 'Email',
          placeholder: 'example@acme.com',
          inputName: 'email',
          type: 'email',
          vModel: '',
          class: this.isEmailValid ? '' : 'invalidInput',
          // pattern: new RegExp(/\S+@\S+\.\S+/),
        },
        {
          label: 'Password',
          placeholder: '••••••••',
          inputName: 'pass',
          type: this.isPasswordVisible ? 'text' : 'password',
          vModel: '',
          // pattern: new RegExp(/(?=.*[!@#$%^&*])(?=.*[A-Z].*[A-Z])[0-9a-zA-Z!@#$%^&*]{8,}/),
        },
        {
          label: 'Repeat password',
          placeholder: '••••••••',
          inputName: 'repeatpass',
          type: this.isPasswordVisible ? 'text' : 'password',
          vModel: '',
          // pattern: new RegExp(/(?=.*[!@#$%^&*])(?=.*[A-Z].*[A-Z])[0-9a-zA-Z!@#$%^&*]{8,}/),
        },
      ],
      msg: 'Sign Up',
      isHintVisible: false,
      isPasswordVisible: false,
      isEmailValid: true,
      hintText: 'Password must contain 8+ symbols, 1 special and 2 capital letters',
      // savedUser: {
      //   userName: localStorage.setItem('userName', this.fields[0].vModel),
      // },
    };
  },
  components: {
    Input, ButtonRectangle,
  },
  methods: {
    checkForm() {
      if (!this.fields[1].vModel.includes('@')) {
        this.isEmailValid = false;
      }
    },
  },
};
</script>

<style>
.container {
    margin: 0 auto;
}
form {
    position: relative;
    margin: 0 auto;
    max-width: 270px;
    background: #FFFFFF;
    border-radius: 40px;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.hint {
  position: absolute;
  border: none;
  background: none;
  background-image: url('../assets/question.png');
  background-repeat: no-repeat;
  background-position: center;
  padding: 7px;
  top: 180px;
  right: 40px;
  cursor: pointer;
  opacity: 0.3;
}

.hint-text {
  font-weight: normal;
  font-size: 10px;
  line-height: 14px;
  text-align: center;
  letter-spacing: -0.4px;
  color: #F3F3F3;
  background:  #1E1A3E;
  box-shadow: 0px 5.44862px 13.6215px rgba(0, 0, 0, 0.1);
  border-radius: 8px;
  padding: 7px 11px 5px;
  position: absolute;
  top: 130px;
  right: 25px;
  max-width: 65%;
}

.hint-text:before {
  content: '';
  position: absolute;
  right: 21px;
  top: 26px;
  width: 15px;
  height: 15px;
  background: #1E1A3E;
  transform:rotate(-45deg);
  transform-origin: top right;
  border-radius : 0 0 0 3px;
}

.passbutton {
  background: none;
  border: none;
  padding: 10px;
  position: absolute;
  content: '';
  background: url('../assets/eye.png') no-repeat center;
  right: 30px;
  top: 205px;
  cursor: pointer;
}

.repeatPassbutton {
  top: 282px;
}

.passbutton:first-child {
  border: 2px solid yellow;
}

.blue-button button {
  background-color: #1E1A3E;
  color: #FFFFFF;
  padding-left: 50px;
  padding-right: 50px;
  margin-top: 40px;
  margin-bottom: 20px;
}

.invalidInput {
  background: #FF6683;
  opacity: 0.2;
  position: relative;
}

.invalidInput::after {
  position: absolute;
  border: 2px solid red;
  content: 'Enter valid email';
  top: 0;
  left: 0;
  width: 30px;
  height: 30px;
}
</style>
