
<script>
    import Navbar from '$lib/components/Navbar.svelte'
    import Footer from '$lib/components/Footer.svelte'
    import RequestForm from '$lib/components/request_form/RequestForm.svelte';
</script>




<header>
    <Navbar/>
</header>
<main>
    <div class="w-screen bg-zinc-100 flex justify-center">
        <!--
            bg-amber-200
        -->
        <div class="flex flex-col items-start w-full max-w-[1400px] px-[100px] py-[50px]">
            <div class="flex flex-col items-center w-full">
                <RequestForm/>
            </div>
        </div>
    </div>
</main>
<footer>
    <Footer/>
</footer>




<style>
</style>