<template>
  <div>
    <input @change="$emit('input')" />
    <button @click.prevent="$emit('test')">
      <slot />
    </button>
  </div>
</template>

<script>
export default defineComponent({
  name: 'BaseButton',
})
</script>
