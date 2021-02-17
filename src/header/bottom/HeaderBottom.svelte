<div class="container">
    <div class="header-bottom">
        <div class="left">
            <a href="">
                <img src="https://uztelecom.uz/images/logo.svg" alt="uztelecom logo">
            </a>
        </div>
        <div class="right">
            <nav>
                <ul>
                    {#each navItems as item}
                        <li class="dropdown">
                            <a href="">{item.name}</a>
                        </li>
                    {/each}
                </ul>
            </nav>
        </div>
    </div>
</div>

<script>
    import {navItems} from "./navItem";
</script>

<style type="text/scss" src="./header-bottom.scss">
</style>