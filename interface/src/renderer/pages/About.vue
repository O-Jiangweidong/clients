<template>
  <div>
    <img id="logo" src="@/assets/Title.png" alt=""/>
    <p>{{ $t('Common.ToecsecClient') }}</p>
    <p>{{ $t('AboutUs.Version') }}：v2.1.4</p>
  </div>
</template>

<script>
export default {
  name: "AboutPage",
  components: {},
  setup() {}
}
</script>

<style lang="scss" scoped>
div {
  width: 100%;
  height: 100%;
  text-align: center;
  color: #e1e1e1e1;

  p {
    font-size: 15px;
  }

  a {
    line-height: 50px;
    margin: 0 15px;
    color: #3f83cc;
  }

  #logo {
    margin-top: 80px;
    width: 200px;
  }
}
</style>
