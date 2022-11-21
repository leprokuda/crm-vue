<template>

  <div class="content">

    <div class="content__page">
      <h2 class="content__title">{{ title }}</h2>
    </div>

  </div>

</template>

<script lang="ts">

export default {
  name: 'CrmContent',
  props: ['title']
}

</script>

<style lang="scss">

  .content {
    background: #FFFFFF;
    border: 1px solid #BCDFE7;
    border-radius: 10px;
    height: 100%;
  }

  .content__page {
    padding: 20px;
  }

  .content__title {
    font-size: 36px;
    margin: auto;
    text-align: center;
  }

</style>
