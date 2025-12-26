<script>
    import Navbar from '$lib/components/Navbar.svelte'
    import Footer from '$lib/components/Footer.svelte'
    import { STRINGS } from '$lib/strings';
    import PrivacyPolicyContent from '$lib/components/PrivacyPolicyContent.svelte';
</script>




<header>
    <Navbar/>
</header>

<main>
    <!-- Page background -->
    <div class="w-screen bg-zinc-100 flex justify-center">
        <!-- Main content column -->
        <div class="flex flex-col  items-center w-full max-w-[1400px] px-[100px] py-[50px] bg-amber-200">
            <!-- Privacy policy column  -->
            <div class="flex flex-col items-center w-full max-w-[600px] bg-amber-700">
                <PrivacyPolicyContent/>
            </div>
        </div>
    </div>
</main>

<footer>
    <Footer/>
</footer>




<style>
</style>