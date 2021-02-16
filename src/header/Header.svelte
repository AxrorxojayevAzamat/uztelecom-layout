<header class="header">
    <HeaderTop></HeaderTop>
    <HeaderBottom></HeaderBottom>
</header>

<script>
    import HeaderTop from "./HeaderTop.svelte";
    import HeaderBottom from "./HeaderBottom.svelte";
</script>

<style type="text/scss">

  header {
    display: flex;
    flex-direction: column;

    /*TOP*/


    /*BOTTOM*/
    .header-bottom {

    }
  }

  @media only screen and (max-width: 992px) {
    .header-top {
      display: none;
    }
  }

</style>