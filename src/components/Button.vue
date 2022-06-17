<template>
  <button @click="onClick()" :style="{ background: color }" class="btn">{{ title }}</button>
</template>

<script>
export default {
  props: ["title", "color"],
  methods: {
    onClick(){
       this.$emit('btn-click')
    }
  },
};
</script>

<style lang="scss" scoped></style>
