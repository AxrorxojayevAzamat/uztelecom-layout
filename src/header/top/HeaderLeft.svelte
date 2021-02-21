<div class="left">
    <ul>
        {#each tabItems as item, i}
            <li class:active='{ n === i }'>
                <a href="#" on:click={() => { n = i }}>{item}</a>
            </li>
        {/each}
    </ul>
</div>

<script>
    let tabItems = ['Jismoniy shaxslarga', 'Biznesga', 'Operatorlarga', 'Agentlarga'], n = 0
</script>

<style type="text/scss">
  @import "header-top-mixin";

  .left {
    ul {
      li.active {
        a {
          background-color: #fff;
          color: rgba(33, 47, 61, .6);
        }
      }

      li {
        display: inline-block;
        vertical-align: top;

        a {
          @include headerItem(18px, 20px, 12px, 12px);

          &:hover {
            color: #212f3d;
          }
        }
      }
    }
  }
</style>