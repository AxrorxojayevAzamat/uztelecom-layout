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
  }
</style>