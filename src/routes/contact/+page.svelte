<script>
    import Navbar from '$lib/components/Navbar.svelte'
    import Footer from '$lib/components/Footer.svelte'
    import ContactComponent from '$lib/components/contact/ContactComponent.svelte';
</script>




<header>
    <Navbar/>
</header>
<main>
    <!-- Page background -->
    <div class="w-screen bg-zinc-100 flex justify-center">
        <!-- Main content column 
            bg-amber-200
        -->
        <div class="flex flex-col  items-center w-full max-w-[1400px] px-[100px] py-[50px]">    
            <ContactComponent/>
        </div>
    </div>
</main>
<footer>
    <Footer/>
</footer>




<style>
</style>