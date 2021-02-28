<div class="breadcrumb">
    <i class="bg" style=" background-image: {imgUrl}"></i>
    <div class="container">
        <div class="wrap">
            <nav>
                <ul>
                    {#each breadcrumbs as breadcrumb, i}
                        <li>
                            {#if i === 0}
                                <a href="">{breadcrumb.title}</a>
                            {:else}
                                <span>{breadcrumb.title}</span>
                            {/if}
                        </li>
                    {/each}
                </ul>
            </nav>
            <div class="mainTitle">
                <h1>{breadcrumbs[breadcrumbs.length-1].title}</h1>
            </div>
        </div>
    </div>
</div>

<script>
    let title = 'Boshqaruv organlari', imgUrl = 'url(https://uztelecom.uz/images/breadcrumbs-bg.jpg)',
        breadcrumbs = [{title: 'Bosh sahifa'}, {title: 'Kompaniya haqida'}, {title: 'Boshqaruv organlari'}]
</script>

<style type="text/scss">
    .breadcrumb {
      background: #228bd6;
      padding: 35px 0;
      position: relative;
      .bg {
        display: block;
        position: absolute;
        top: 0;
        right: 0;
        width: 100%;
        height: 100%;
        background-position: center;
        background-repeat: no-repeat;
        background-size: cover;
      }
      .container {
        max-width: 1440px;
        margin: 0 auto;
        width: 100%;
        position: relative;
        z-index: 1;
        .wrap {
          padding: 0 15px;
          nav {
            display: block;
            overflow: auto;
            ul {
              li {
                list-style: none;
                display: inline-block;
                vertical-align: middle;
                padding-right: 18px;
                margin-right: 12px;
                position: relative;
                white-space: nowrap;
                a {
                  display: block;
                  font: 400 12px/18px Montserrat,sans-serif;
                  color: hsla(0,0%,100%,.5);
                  text-decoration: none;
                  text-transform: uppercase;
                  transition: color .25s ease 0s;
                  &:hover {
                    color: #fff;
                  }
                }
                span {
                  font: 400 12px/18px Montserrat,sans-serif;
                  color: hsla(0,0%,100%,.5);
                  text-transform: uppercase;
                }
                &::after {
                  position: absolute;
                  content: ">";
                  top: 0;
                  right: 0;
                  font-size: 12px;
                  line-height: 15px;
                  color: hsla(0,0%,100%,.5);
                }
                &:last-child {
                  padding-right: 0;
                  margin-right: 0;
                  &::after {
                    content: "";
                  }
                }
              }
            }
          }
          .mainTitle {
            h1 {
              display: inline-block;
              font: 700 48px/60px Montserrat,sans-serif;
              color: #fff;
            }
          }
        }


      }
    }
</style>