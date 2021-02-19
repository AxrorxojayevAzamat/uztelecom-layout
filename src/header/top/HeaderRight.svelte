<div class="right">
    <ul class="region">
        <li>
            <HeaderDropdown {...ddData.lang}/>
        </li>
    </ul>
    <div class="cabinet">
        <HeaderDropdown {...ddData.cabinet}/>
    </div>
</div>

<script>
    import HeaderDropdown from "./HeaderTopDropdown.svelte";

    let ddData = {
        lang: {name: 'O\'zbek', icon: 'globe-americas', data: ['Русский', 'O\'zbek', 'English']},
        cabinet: {name: 'Shaxsiy kabinet', icon: 'user-alt', data: ['Shaxsiy kabinet', 'Virtual ofis']}
    }
</script>

<style type="text/scss">
  @import "header-top-mixin";

  .right {
    @include flexMargin(0, -20px, space-between);
    align-items: center;
    min-width: 300px;

    ul.region {
      line-height: 0;
      margin: 0 -12px;

      li {
        @include headerDropdownItem(inline-block);
      }
    }

    .cabinet {
      position: relative;
    }
  }

</style>