<script>
  import TheHeader from "./components/TheHeader.vue";
  import TheMain from "./components/TheMain.vue";
  import TheFooter from "./components/TheFooter.vue";
  import FixedButton from "./components/FixedButton.vue";

  export default{
    components:{
      TheHeader,
      TheMain,
      TheFooter,
      FixedButton
    }
  }
</script>

<template>
  <FixedButton></FixedButton>
  <TheHeader></TheHeader>
  <TheMain></TheMain>
  <TheFooter></TheFooter>
</template>

<style lang="scss">

</style>
