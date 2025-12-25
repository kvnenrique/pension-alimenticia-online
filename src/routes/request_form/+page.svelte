
<script>
    import Navbar from '$lib/components/Navbar.svelte'
    import Footer from '$lib/components/Footer.svelte'
    import { Button }  from 'flowbite-svelte'
    import { STRINGS } from '$lib/strings';
</script>




<header>
    <Navbar/>
</header>
<main>
    <div class="w-screen bg-zinc-100 flex justify-center">
        <div class="flex flex-col items-start w-full max-w-[1400px] px-[100px] py-[50px] bg-amber-200">
            <p class="text-4xl"> Request form</p>
        </div>
    </div>
</main>
<footer>
    <Footer/>
</footer>




<style>
</style>