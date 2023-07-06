<template>
  <button @click="$emit('clickSubmit')" type="button">{{ text }}</button>
</template>
  
  <script setup>
const emit = defineEmits(["clickSubmit"]);
const props = defineProps({
  text: { type: String, default: "✉︎同意して新規登録する(無料)" },
});
</script>
  
  <style lang="scss" scoped>
button {
  background-color: #f86986;
  border-radius: 10px;
  border: none;
  padding: 15px 20px;
  color: white;
  font-weight: bold;
}
</style>


