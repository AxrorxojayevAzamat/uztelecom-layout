<div class="top">
    <div class="left">
        <FooterLeft/>
    </div>
    <div class="right">
        <FooterRight/>
    </div>
</div>

<script>
    import FooterLeft from "./FooterLeft.svelte";
    import FooterRight from "./FooterRight.svelte";
</script>

<style type="text/scss">
    .top {
      font-size: 0;
      line-height: 0;
      padding-bottom: 40px;
      .left {
        width: 66.66666667%;
        display: inline-block;
        vertical-align: top;
        @media only screen and (max-width: 992px) {
          display: none;
        }
        @media only screen and (max-width: 1330px) {
          width: 100%;
        }
      }
      .right {
        width: 33.33333333%;
        display: inline-block;
        vertical-align: top;
        @media only screen and (max-width: 1330px) {
          width: 100%;
        }
      }
    }
</style>