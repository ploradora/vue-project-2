<template>
  <div class="card">
    <slot></slot>
  </div>
</template>

<style scoped lang="scss">
.card {
  width: 90%;
  max-width: 400px;
  border-radius: 20px;
  margin: 8rem 0;
  background-color: #fff;
  box-shadow: 0px 39px 34px 4px rgba(0, 0, 0, 0.3);

  @media only screen and(min-width: 830px) {
    position: relative;
    margin: unset;
    display: flex;
    width: 80%;
    max-width: 800px;
  }
}
</style>
