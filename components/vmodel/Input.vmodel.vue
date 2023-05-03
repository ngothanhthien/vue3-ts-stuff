<script setup lang="ts">
  const props = defineProps({
    modelValue: {
      value: String,
      required: true
    }
  })
const emit = defineEmits(['update:modelValue'])
function updateModelValue(e: Event) {
  const el = e.target as HTMLInputElement
  emit('update:modelValue', el.value)
}
</script>

<template>
  <div>
    <label for="first_name" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Input V-model</label>
    <input 
    type="text"
    class="w-96 bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 p-2.5" 
    :value="modelValue"
    @input="updateModelValue">
  </div>
</template>
