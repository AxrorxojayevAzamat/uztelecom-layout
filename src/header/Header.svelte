<header class="header">
    <HeaderTop/>
    <HeaderBottom/>
</header>

<script>
    import HeaderTop from "./top/HeaderTop.svelte";
    import HeaderBottom from "./bottom/HeaderBottom.svelte";
</script>

<style type="text/scss">
  header {
    display: flex;
    grid-area: header;
    flex-direction: column;
    @media only screen and (max-width: 992px) {
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      background-color: #fff;
      z-index: 99999;
    }
  }
</style>