
<footer>
    <div class="container">
        <div class="wrap">
            <FooterTop/>
            <FooterBottom/>
        </div>
    </div>
</footer>

<script>
    import FooterTop from "./top/FooterTop.svelte";
    import FooterBottom from "./FooterBottom.svelte";
</script>

<style type="text/scss">
  footer {
    background-color: #fff;
    border-top: 5px solid #228bd6;

    .container {
      max-width: 1440px;
      margin: 0 auto;
      width: 100%;
      padding: 70px 0;

      .wrap {
        padding: 0 15px;
      }
    }
  }
</style>