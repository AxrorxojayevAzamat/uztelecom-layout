<a href="" on:mouseover={() => {visible = true}} on:mouseleave={() => {visible=false}} class="header-item">
    <i class="fas fa-{icon}"></i>
    {name}
</a>
{#if visible}
    <ul class="header-top-dropdown" on:mouseover={() => {visible = true}} on:mouseleave={() => {visible=false}}
        transition:fly={{y: 10, delay: 100}}>
        {#each data as d}
            <li><a href="">{d}</a></li>
        {/each}
    </ul>
{/if}

<script>
    import {fly} from 'svelte/transition';

    export let data = []
    export let visible = false, icon = '', name = ''
</script>

<style type="text/scss">
  @import "header-top-mixin";

  a {
    @include headerItem(9px, 12px, 12px, 24px);
    @include headerItemHover(24px);
  }

  ul.header-top-dropdown {
    min-width: 100%;
    position: absolute;
    top: 40px;
    z-index: 4;
    overflow: hidden;
    background-color: #fff;
    box-shadow: 0 10px 30px 0 rgba(56, 56, 55, .2);
    border-bottom-left-radius: 4px;
    border-bottom-right-radius: 4px;
    border-top: 2px solid #228bd6;
    transition: all .3s ease 0s;

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

</style>

