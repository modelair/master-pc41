<template>
  <div class="rule">
    <div class="rule-text"></div>
    <slot></slot>
    <div class="rule-text"></div>
  </div>
</template>

<script setup>

</script>

<style scoped lang="scss">
.rule {
  display: flex;
  flex-direction: row;
  width: 100%;
  align-content: center;
  flex-grow: 1;
  align-items: center;
  gap: 1em;
}
.rule-text {
  flex-grow: 1;
  border: 2px solid;
}
</style>
