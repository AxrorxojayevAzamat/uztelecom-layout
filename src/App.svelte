<MobileMenu/>
<input type="checkbox" id="mobilemenu" name="mobilemenu">

<div class="wrapper">
    <Header/>
    <Main>
        <Home/>
    </Main>
    <Footer/>
</div>

<script>
    import Header from "./header/Header.svelte";
    import Main from "./main/Main.svelte";
    import Footer from "./footer/Footer.svelte";
    import MobileMenu from "./components/mmenu/MobileMenu.svelte";
    import Home from "./home/Home.svelte";
</script>
