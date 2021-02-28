<div class="content">
    <div class="container">
        <div class="wrap">
            <slot></slot>
        </div>
    </div>
</div>


<style type="text/scss">

  .content {
    padding: 60px 0 90px;
    //font-size: 0;
    //line-height: 0;

    .container {
      max-width: 1440px;
      margin: 0 auto;
      width: 100%;

      .wrap {
        padding: 0 15px;
      }
    }
  }
</style>