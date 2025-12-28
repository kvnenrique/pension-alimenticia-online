
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
            <p class="text-4xl">¿No te da la pensión para tus hijos?</p>
            
            <Button
                size="xl"
                class="inline-flex"
                href="/request_form"    
            >
                {STRINGS.start_procedure}
            </Button>    
            
            <p class="text-4xl">¡Obtén una orden de descuento judicial en menos de 48 horas!</p>
        </div>
    </div>
</main>
<footer>
    <Footer/>
</footer>




<style>
</style>