<div class="header-top">
    <div class="wrap">
        <HeaderLeft/>
        <HeaderMiddle/>
        <HeaderRight/>
    </div>
</div>

<script>
    import HeaderLeft from "./HeaderLeft.svelte";
    import HeaderMiddle from "./HeaderMiddle.svelte";
    import HeaderRight from "./HeaderRight.svelte";
</script>

<style type="text/scss">
  @import "header-top-mixin";

  .header-top {
    background-color: #f1f8ff;
    padding: 5px 0 0;

    .wrap {
      @include flexMargin(0, auto, space-between);
      max-width: 1440px;
      width: 100%;
    }
  }

  @media only screen and (max-width: 992px) {
    .header-top {
      display: none;
    }
  }
</style>