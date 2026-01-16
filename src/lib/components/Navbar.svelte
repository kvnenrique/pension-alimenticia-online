<script lang="ts">
    import { STRINGS } from "$lib/strings";
    import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from "flowbite-svelte";
</script>

<Navbar class="dark dark:bg-primary-700">
    <NavBrand href="/">
        <!-- <img src="/images/flowbite-svelte-icon-logo.svg" class="me-3 h-6 sm:h-9" alt="Flowbite Logo" />  -->
        <span class="self-center text-xl font-semibold whitespace-nowrap text-white">{STRINGS.appName}</span>
    </NavBrand>
    <NavHamburger />
    <NavUl>
        <NavLi class="navlink" href="/">{STRINGS.home}</NavLi>
        <NavLi class="navlink" href="/about_us">{STRINGS.about_us}</NavLi>
        <NavLi class="navlink" href="/privacy_policy">{STRINGS.privacy_policy}</NavLi>
        <NavLi class="navlink" href="/contact">{STRINGS.contact}</NavLi>
    </NavUl>
</Navbar>