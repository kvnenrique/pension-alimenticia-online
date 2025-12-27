
<script>
    import Navbar from '$lib/components/Navbar.svelte'
    import Footer from '$lib/components/Footer.svelte'
    import RequestForm from '$lib/components/request_form/RequestForm.svelte';
    import { Button }  from 'flowbite-svelte'
    import { STRINGS } from '$lib/strings';
</script>




<header>
    <Navbar/>
</header>
<main>
    <div class="w-screen bg-zinc-100 flex justify-center">
        <div class="flex flex-col items-start w-full max-w-[1400px] px-[100px] py-[50px] bg-amber-200">
            <RequestForm/>
        </div>
    </div>
</main>
<footer>
    <Footer/>
</footer>




<style>
</style>