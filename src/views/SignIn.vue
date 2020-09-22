<template>
    <div>
        <h1>Sign In</h1>
        <SignInForm />
        <p class="have-account">Don’t have an account yet?
          <br>
          <router-link to="/signup">Sign Up</router-link>
        </p>
    </div>
</template>

<script>
import SignInForm from '@/components/SignInForm.vue';

export default {
  data() {
    return {
      savedUser: {
        userName: 'example',
        userPass: 'example',
      },
    };
  },
  components: {
    SignInForm,
  },
};
</script>

<style>
.have-account {
  margin-top: 40px;
  margin-bottom: 30px;
  text-align: center;
  font-weight: 500;
  font-size: 14px;
  line-height: 20px;
  color: #1E1A3E;
}

.have-account a:visited {
  color: #1E1A3E;
}
</style>
