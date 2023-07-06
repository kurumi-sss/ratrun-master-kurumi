<template>
  <div class="input">
    <label>{{ text }}</label>
    <br />
    <input
      :type="type"
      name="email"
      :placeholder="placeholder"
      :required="required"
    />
  </div>
</template>
    
<script setup>
const props = defineProps({
  text: { type: String, default: null },
  type: { type: String, default: null },
  placeholder: { type: String, default: null },
  required: { type: Boolean, default: false },
});
</script>
    
    <style lang="scss">
.input {
  input {
    width: 100%;
    padding: 30px;
    box-sizing: border-box;
    border: 1px solid gray;
    border-radius: 20px;
  }
  label {
    font-weight: bold;
  }
}
</style>