<div class="header-top">
    <div class="wrap">
        <div class="left">
            <ul>
                {#each tabItems as item}
                    <li class=""><a href="">{item}</a></li>
                {/each}
            </ul>
        </div>
        <div class="middle">
            <a href="" class="specialFeatureBtn">
                <i class="fas fa-glasses"></i>
                maxsus imkoniyatlar
            </a>
        </div>
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
    </div>
</div>

<script>
    import HeaderDropdown from "./HeaderDropdown.svelte";

    let tabItems = ['Jismoniy shaxslarga', 'Biznesga', 'Operatorlarga', 'Agentlarga']
    let ddData = {
        lang: {name: 'O\'zbek', icon: 'globe-americas', data: ['Русский', 'O\'zbek', 'English']},
        cabinet: {name: 'Shaxsiy kabinet', icon: 'user-alt', data: ['Shaxsiy kabinet', 'Virtual ofis']}
    }
</script>

<style type="text/scss" src="./header-top.scss">
</style>