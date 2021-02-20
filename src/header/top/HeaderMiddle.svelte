<div class="middle">
    <a href="" class="specialFeatureBtn">
        <span class="fas fa-{icon}"></span>
        {middleText}
    </a>
    <div>
        <span class="element">AAAAA</span>
    </div>
</div>

<script>
    let icon = 'glasses', middleText = 'maxsus imkoniyatlar'
</script>

<style type="text/scss">
  @import "header-top-mixin";

  .middle {
    display: inline-block;
    position: relative;
    a.specialFeatureBtn {
      @include headerIcon(18px);
      @include headerItem(12px, 20px, 12px, 24px);
    }
    div {
      @include headerDropdown(3, 58px);
      span.element {
        position: relative;
        height: 50px;
      }
    }
    &:hover {
      a.specialFeatureBtn {
        background-color: #fff;
        color: #228bd6;
        span {
          color: #228bd6;
        }
      }
      div {
        opacity: 1;
        top: 45px;
        visibility: visible;
      }
    }
  }
</style>