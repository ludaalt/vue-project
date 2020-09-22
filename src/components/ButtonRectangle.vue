<template>
  <div>
    <button class="rect-button">{{msg}}</button>
  </div>
</template>

<script>
export default {
  name: 'ButtonRectangle',
  props: ['msg'],
};
</script>

<style>
.rect-button {
  cursor: pointer;
  border: none;
  border-radius: 50px;
  background-color: #fff;
  padding: 10px 25px;
  font-weight: 500;
  font-size: 14px;
  line-height: 20px;
  text-align: center;
  color: #000000;
}
</style>
