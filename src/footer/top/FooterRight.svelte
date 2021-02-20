<div class="wraps">
    <h3>{title}</h3>

    <ul class="contact">
        {#each contacts as contact}
            <li>
                <i class="fas fa-phone-alt"></i>
                <a href="" class="phone">{contact.number}</a>
                <span class="note">{contact.note}</span>
            </li>
        {/each}
        <li>
            <i class="fa fa-envelope"></i>
            <a href="">Murojaat yuborish</a>
        </li>
    </ul>

    <ul class="socialLinks">
        {#each socials as social}
            <li>
                <a href="{social.link}">
                    <i class="fab fa-{social.icon}"></i>
                </a>
            </li>
        {/each}
    </ul>

    <ul class="downloadLinks">
        {#each downloads as download}
            <li>
                <a href="{download.link}">
                    <img src="/images/{download.img}.jpg" alt="">
                </a>
            </li>
        {/each}
    </ul>
</div>

<script>
    import {contacts, socials, downloads} from "./call-social";

    let title = 'Biz bilan bog\'laning'
</script>

<style type="text/scss">
  .wraps {
    padding-left: 120px;

    @media only screen and (max-width: 1330px) {
      padding-left: 0;
    }

    h3 {
      font: 700 18px/18px Montserrat, sans-serif;
      color: #212f3d;
      margin-bottom: 30px;
    }

    .contact {
      li {
        list-style: none;
        position: relative;
        padding-left: 40px;
        margin-bottom: 30px;

        i {
          position: absolute;
          top: 0;
          left: 0;
          font-size: 24px;
          color: #8d959d;
        }

        .phone {
          font: 700 24px/24px Montserrat, sans-serif;
          color: #212f3d;
          text-decoration: none;
          transition: color .2s ease 0s;
          &:hover {
            color: #228bd6;
          }
        }

        .note {
          display: block;
          font: 400 14px/22px Montserrat, sans-serif;
          color: #8d959d;
        }

        a {
          font: 400 14px/22px Montserrat, sans-serif;
          color: #8d959d;
          text-decoration: none;
          transition: color .2s ease 0s;
        }
      }
    }

    .socialLinks {
      margin: 0 -5px;

      li {
        list-style: none;
        display: inline-block;
        vertical-align: middle;
        padding: 0 5px;

        a {
          text-decoration: none;

          i {
            font-size: 20px;
            color: #8d959d;
            transition: color .2s ease 0s;
          }

          &:hover, &:focus {
            color: #166dba;

            i {
              color: #228bd6;
            }
          }
        }
      }
    }

    .downloadLinks {
      position: relative;
      display: inline-block;
      margin-top: 25px;
      li {
        display: inline-block;
        margin-right: 15px;
        a {
          color: #228bd6;
          text-decoration: none;
          img {
            width: 120px;
            height: 50px;
            border-radius: 5px;
          }
        }
      }
    }

  }
</style>