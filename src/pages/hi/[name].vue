<script setup lang="ts">
const props = defineProps<{ name: string }>()
const router = useRouter()
</script>

<template>
  <div>
    <div i-carbon-pedestrian inline-block text-4xl data-cursor="block" />
    <p>
      Hi, {{ props.name }}
    </p>
    <p text-sm op50>
      <em>Dynamic route!</em>
    </p>

    <div>
      <div data-cursor="block" m-3 mt-8 cursor-none text-sm btn @click="router.back()">
        Back
      </div>
    </div>
  </div>
</template>
