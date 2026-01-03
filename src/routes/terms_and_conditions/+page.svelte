<script>
    import Navbar from '$lib/components/Navbar.svelte'
    import Footer from '$lib/components/Footer.svelte'
    import TermsAndConditionsContent from '$lib/components/terms_and_conditions/TermsAndConditionsContent.svelte';
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
            <!-- Privacy policy column 
                bg-amber-700
              -->
            <!-- <div class="flex flex-col items-center w-full max-w-[600px] "> -->
                <TermsAndConditionsContent/>
            <!-- </div> -->
        </div>
    </div>
</main>
<footer>
    <Footer/>
</footer>




<style>
</style>