<template>
  <div>
    <button class="button-round"></button>
  </div>
</template>

<script>
export default {
  name: 'ButtonRound',
};
</script>

<style>
.button-round {
  cursor: pointer;
  padding: 20px;
  border: none;
  border-radius: 50px;
  background: none;
  background-color: #1E1A3E;
  background-image: url('../assets/arrow.png');
  background-repeat: no-repeat;
  background-position: center;
}
</style>
