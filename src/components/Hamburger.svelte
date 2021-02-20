<script>
    export let open = false
</script>

<button class="hamburger-btn" class:open on:click={() => open = !open}>
    <svg width=28 height=21>
        <line id="top" x1=0 y1=5 x2=32 y2=5/>
            <line id="middle" x1=0 y1=12 x2=32 y2=12/>
                <line id="bottom" x1=0 y1=19 x2=32 y2=19/>
    </svg>
</button>

<style type="text/scss">

  svg {
    min-height: 24px;
    transition: transform 0.3s ease-in-out;

    line {
      stroke: currentColor;
      stroke-width: 2;
      transition: transform 0.3s ease-in-out;
      color: #228bd6;
    }
  }

  button {
    z-index: 20;
    border: none;
    background-color: #fff;

    &:focus {
      outline: none;
    }
  }

  .open {
    line {
      transform: scale(1.35)
    }

    #top {
      transform: translate(4px, -1px) rotate(40deg)
    }

    #middle {
      opacity: 0;
    }

    #bottom {
      transform: translate(-11px, 9px) rotate(-40deg)
    }
  }

</style>