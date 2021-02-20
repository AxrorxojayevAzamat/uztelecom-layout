<div class="container">
    <div class="header-bottom">
        <div class="left">
            <a href="">
                <img src="https://uztelecom.uz/images/logo.svg" alt="uztelecom logo">
            </a>
        </div>
        <div class="right">
            <HeaderNav/>
        </div>
    </div>
</div>

<script>
    import HeaderNav from "./HeaderNav.svelte";


</script>

<style type="text/scss">
  .container {
    max-width: 1440px;
    margin: 0 auto;
    width: 100%;

    .header-bottom {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 6px 15px;
      //line-height: 0;
      position: relative;

      .left {
        max-width: 270px;

        a {
          display: block;
          text-decoration: none;

          img {
            display: inline-block;
            height: 31px;
            @media only screen and (max-width: 992px) {
              max-width: 140px;
            }
          }

        }
      }

      .right {
        display: flex;
        align-items: center;
        justify-content: space-between;

        .searchBtn {
          text-decoration: none;
          display: inline-block;
          padding-left: 0;
          position: absolute;
          right: 0;

          &:active {
            color: #212f3d;
          }

          span {
            font-size: 16px;
            color: #212f3d;
          }
        }
      }
    }

  }
</style>