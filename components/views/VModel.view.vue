<script setup lang="ts">
import InputVModel from '../vmodel/Input.vmodel.vue';
const message = ref('hello')

</script>
<template>
  <div>V-model</div>
  <div>
    <InputVModel v-model="message" />
    {{ message }}
  </div>
</template>
