<script lang="ts" setup>
const name = ref('')
const router = useRouter()

function go() {
  if (name) {
    router.push({
      name: 'hello',
      params: { name: name.value },
    })
  }
}
</script>

<template>
  <div>
    <i i-ph:file-vue text-4xl text-primary-600 />
    <div mt-4>
      <p>
        Opinionated Vue starter template
      </p>
      <p opacity-75 text-xs font-mono leading-relaxed mt-3>
        UnoCSS . Pinia . VueUse . CSS Nesting . Auto imports . File based routing . ESLint
      </p>
    </div>
  </div>

  <div flex flex-col gap-4 items-center>
    <div class="bg-blue-400/50 hover:animate-pul" />
    <TheInput
      v-model="name"
      placeholder="What's your name?"
      autocomplete="false"
      @keydown.enter="go"
    />
    <button
      btn text-sm uppercase
      :disabled="!name"
      @click="go"
    >
      go
    </button>
  </div>
</template>
