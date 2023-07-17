<script setup lang="ts" generic="T extends any, O extends any">
import { useCursor } from 'ipad-cursor/vue'

useCursor()
defineOptions({
  name: 'IndexPage',
})

const name = ref('')

const router = useRouter()
function go() {
  if (name.value)
    router.push(`/hi/${encodeURIComponent(name.value)}`)
}
</script>

<template>
  <div>
    <div i-carbon-campsite inline-block text-4xl data-cursor="block" />
    <p>
      <a rel="noreferrer" href="https://github.com/antfu/vitesse-lite" target="_blank">
        Vitesse Lite
      </a>
    </p>
    <p>
      <em text-sm op75 data-cursor="text">Opinionated Vite Starter Template</em>
    </p>

    <div py-4 />

    <TheInput
      v-model="name"
      placeholder="What's your name?"
      autocomplete="false"
      data-cursor="text"
      @keydown.enter="go"
    />

    <div>
      <div
        data-cursor="block"
        class="m-3 text-sm btn"
        :disabled="!name"
        cursor-none
        @click="go"
      >
        Go
      </div>
    </div>
  </div>
</template>
