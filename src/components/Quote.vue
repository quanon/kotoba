<template lang="pug">
  blockquote
    p(v-html="body")
    cite {{ source }}
</template>

<script>
  export default {
    props: ['body', 'source']
  };
</script>

<style lang="scss" scoped>
  $blockquote-background-color: #f5f5f5;
  $blockquote-font-color: #777777;
  $cite-font-color: #888888;
  $quote-left-color: #9dd4ff;

  blockquote {
    font-family: "Mplus 1p";
    position: relative;
    padding: 1.0rem 1.5rem 1.0rem 6.0rem;
    box-sizing: border-box;
    font-style: italic;
    background: $blockquote-background-color;
    color: $blockquote-font-color;
    border-left: 0.4rem solid $quote-left-color;
    box-shadow: 0 0.2rem 0.4rem rgba(0, 0, 0, 0.14);

    &::before {
      display: inline-block;
      position: absolute;
      top: 1.5rem;
      left: 1.5rem;
      vertical-align: middle;
      content: "\f10d";
      font-family: FontAwesome;
      color: $quote-left-color;
      font-size: 3.6rem;
      line-height: 1;
    }

    & > p {
      padding: 0;
      margin: 0.7rem 0;
      line-height: 1.7;
      font-size: 1.6rem;
    }

    & > cite {
      display: block;
      text-align: right;
      color: $cite-font-color;
      font-size: 1.2rem;
    }
  }
</style>
