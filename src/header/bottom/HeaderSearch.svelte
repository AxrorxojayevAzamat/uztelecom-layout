<div class="searchForm" class:active='{show_search}'>
    <form action="">
        <div class="wraps">
            <input type="text" name="quary" placeholder="Qidirub so'rovini kiriting">
            <button type="submit" class="btn">
                <span class="fas fa-search"></span>
            </button>
        </div>
    </form>
</div>

<script>
    export let show_search = false
</script>

<style type="text/scss">
  .searchForm {
    position: absolute;
    right: 40px;
    top: 12px;
    width: 30%;
    opacity: 0;
    visibility: hidden;
    transition: opacity .25s ease 0s, visiblity .25s ease 0s, width .4s ease 0s;
    @media only screen and (max-width: 1500px) {
      top: 8px;
    }
    @media only screen and (max-width: 1240px) {
      top: 1px;
    }
    @media only screen and (max-width: 992px) {
      top: 6px;
    }

    .wraps {
      position: relative;

      input {
        width: 100%;
        padding: 17px 30px 15px;
        font: 400 14px/14px Montserrat, sans-serif;
        color: #8d959d;
        background-color: #f1f8ff;
        display: block;
        box-sizing: border-box;
        border: 0;
        box-shadow: none;
        border-radius: 0;
        -webkit-appearance: none;
        -moz-appearance: none;
        appearance: none;
        &:focus {
          outline: none;
        }

      }

      .btn {
        position: absolute;
        top: 16px;
        right: 20px;
        border: 0;
        border-radius: 0;
        box-shadow: none;
        background-color: transparent;
        cursor: pointer;
        @media (min-width: 1024px) {
          top: 10px !important;
        }

        span {
          font-size: 17px;
          line-height: 17px;
        }
      }
    }
  }

  .active {
    width: calc(100% - 300px);
    opacity: 1;
    visibility: visible;
    @media only screen and (max-width: 1500px) {
      width: calc(100% - 400px);
      opacity: 1;
      visibility: visible;
      right: 100px;
    }
    @media only screen and (max-width: 1170px) {
      width: calc(100% - 300px);
      opacity: 1;
      visibility: visible;
      right: 50px;
    }
    @media only screen and (max-width: 992px) {
      width: calc(100% - 100px);
      right: 90px;
      opacity: 1;
      visibility: visible;
    }


  }
</style>