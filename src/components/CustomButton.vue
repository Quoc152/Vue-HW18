<template>
  <button
    class="inline-flex items-center justify-center px-4 py-2 border border-transparent text-sm font-medium rounded-md shadow-sm text-white bg-blue-600 hover:bg-blue-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-blue-500 disabled:opacity-50 disabled:cursor-not-allowed"
    :disabled="isLoading"
  >
    <slot name="prefix-icon"></slot>
    <span class="mx-2">
      <slot></slot>
    </span>
    <slot name="suffix-icon">
      <Loader2Icon v-if="isLoading" class="animate-spin h-5 w-5" />
    </slot>
  </button>
</template>

<script setup>
import { Loader2Icon } from "lucide-vue-next";

defineProps({
  isLoading: {
    type: Boolean,
    default: false,
  },
});
</script>
