<template>
    <div>
        <h1>Sign Up</h1>
        <SignUpForm />
        <p class="have-account">Already have an account?
          <br>
          <router-link to="/signin">Sign In</router-link>
        </p>
    </div>
</template>

<script>
import SignUpForm from '@/components/SignUpForm.vue';

export default {

  components: {
    SignUpForm,
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
