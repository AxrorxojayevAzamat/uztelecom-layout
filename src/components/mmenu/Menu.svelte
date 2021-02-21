<nav class="menu">
    <ul>
        {#each menus as menu, i}
            <li class:active='{i === n}'>
                <a href="#" on:click={() => { n = i }}>{menu}</a>
            </li>
        {/each}
    </ul>
</nav>

<script>
    let menus = ['Jismoniy shaxslarga', 'Biznesga', 'Operatorlarga', 'Agentlarga'], n = 0
</script>

<style type="text/scss">
  ul {
    font-size: 0;
    line-height: 0;

    li {
      display: block;
      vertical-align: top;

      a {
        font: 500 12px/12px Montserrat, sans-serif;
        color: rgba(33, 47, 61, .6);
        text-decoration: none;
        display: block;
        padding: 8px 10px;
        border-radius: 5px;
        transition: color .2s ease 0s;
      }

      &.active {
        a {
          background-color: #fff;
          color: #212f3d;
        }
      }
    }
  }
</style>