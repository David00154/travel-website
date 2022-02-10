<script lang="ts">
let menuBtnState: boolean = false;
// let navbarSate: boolean = true
import {
    onMount
} from "svelte"

onMount(() => {
    window.onscroll = () => {
        menuBtnState = false
    }
})
</script>

<section class="header">

    <a href="/" class="logo">travel.</a>
    <nav class="navbar" class:active={menuBtnState == true}>
        <a href="/">home</a>
        <a href="/about">about</a>
        <a href="/package">package</a>
        <a href="/book">book</a>
    </nav>
    <div id="menu-btn" on:click="{() => menuBtnState = !menuBtnState}" class="fas" class:fa-times={menuBtnState == true} class:fa-bars={menuBtnState == false}></div>

</section>
