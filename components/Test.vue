<template>
  <div>
    <input @change="test" />
    <button @click.prevent="test">
      <slot />
    </button>
  </div>
</template>

<script>
export default defineComponent({
  name: 'BaseButton',
  methods: {
    test() {
      console.log('test')
    },
  },
})
</script>
