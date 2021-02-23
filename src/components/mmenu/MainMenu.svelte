<nav class="mainMenu">
    <ul>
        <Dropdown menu_items={navItems}/>
    </ul>
    <hr>
    <ul>
        <Dropdown menu_items={second_menu}/>
    </ul>
</nav>

<script>
    import {navItems} from "../../header/bottom/navItem";
    import Dropdown from "./Dropdown.svelte";

    let second_menu = [
        {
            name: 'Kompaniya haqiada',
            open: false,
            children: [
                {name: 'Huquqiy axborot'}
            ]
        },
        {name: 'Korparativ boshqaruv'},
        {name: 'Matbuot-markazi'},
        {name: 'Vakansiyalar'},
        {name: 'Ofislar va filiallar'},
    ]


</script>

<style type="text/scss">
    .mainMenu {
      position: relative;
      ul {
        font-size: 0;
        line-height: 0;
      }
      hr {
        border-top: 1px solid #9ec7e4;
        border-bottom: 0;
        margin-top: 20px;
        margin-bottom: 20px;
        box-sizing: content-box;
        height: 0;
      }
    }
</style>