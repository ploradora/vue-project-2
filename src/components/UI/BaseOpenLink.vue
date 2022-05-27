<template>
  <div :class="mode">
    <slot></slot>
  </div>
</template>

<script>
export default {
    props: ['mode']
};
</script>

<style lang="scss">
.selected {
  .question {
    > p {
      color: #000;
      font-weight: 700;
    }
    .arrow {
        // transform: rotate(180deg);
    }
  }
  .answer {
      display: block;
  }
}
</style>
