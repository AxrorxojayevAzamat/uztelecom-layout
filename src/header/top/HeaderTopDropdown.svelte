<div class="dropdown">
    <a href="" class="header-item">
        <i class="fas fa-{icon}"></i>
        {name}
    </a>
    <ul class="header-top-dropdown">
        {#each data as d}
            <li><a href="">{d}</a></li>
        {/each}
    </ul>
</div>

<script>
    export let data = [], icon = '', name = ''
</script>

<style type="text/scss">
  @import "header-top-mixin";

  a {
    @include headerItem(9px, 12px, 12px, 24px);
    @include headerIcon(24px);
  }

  ul.header-top-dropdown {
    @include headerDropdown(4, 55px);

    li {
      @include headerDropdownItem(block);

      a {
        @include headerItem(9px, 12px, 12px, 24px);

        &:hover {
          background-color: #228bd6;
          color: #fff;
          border-radius: 0;
        }
      }
    }
  }

  .dropdown:hover {
    a {
      background-color: #fff;
      color: #228bd6;
      i {
        color: #228bd6;
      }
    }
    ul.header-top-dropdown {
      opacity: 1;
      top: 40px;
      visibility: visible;
    }
  }
</style>

