<script lang="ts">
    import { STRINGS } from "$lib/strings";
    import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from "flowbite-svelte";
</script>

<Navbar class="bg-pink-900">
    <NavBrand href="/">
        <!-- <img src="/images/flowbite-svelte-icon-logo.svg" class="me-3 h-6 sm:h-9" alt="Flowbite Logo" />  -->
        <span class="self-center text-xl font-semibold whitespace-nowrap dark:text-white">{STRINGS.appName}</span>
    </NavBrand>
    <NavHamburger />
    <NavUl>
        <NavLi href="/">{STRINGS.home}</NavLi>
        <NavLi href="/about_us">{STRINGS.about_us}</NavLi>
        <NavLi href="/privacy_policy">{STRINGS.privacy_policy}</NavLi>
        <NavLi href="/contact">{STRINGS.contact}</NavLi>
    </NavUl>
</Navbar>