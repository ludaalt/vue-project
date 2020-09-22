<template>
<div>
    <p class="form-item" v-for="(field, index) in fields" :key="index">
            <label :for="field.inputName">{{field.label}}
              <input :type="field.type"
              :name="field.inputName"
              :id="field.inputName"
              :placeholder="field.placeholder"
              v-model="field.vModel"
              required
              :pattern="field.pattern"
              :class="field.class">
            </label>
    </p>
</div>
</template>

<script>

export default {
  props: ['fields'],
  components: {
  },
};
</script>

<style>
input {
    width: 230px;
    padding: 10px;
    background: #F3F3FA;
    border: none;
    border-radius: 50px;
}

input::placeholder {
  font-weight: normal;
  font-size: 14px;
  line-height: 0px;
  padding: 7px;
  color: rgba(0, 0, 0, 0.8);
}

input:focus::placeholder {
  color:transparent;
}

label {
  font-weight: 600;
  font-size: 12px;
  line-height: 20px;
  color: rgba(0, 0, 0, 0.8);
  margin-left: 18px;
}

.form-item {
  margin-top: 24px;
  padding-left: 20px;
  padding-right: 20px;
}
</style>
