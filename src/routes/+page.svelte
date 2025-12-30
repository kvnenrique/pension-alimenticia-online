
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
    <!-- Column -->
    <div class="flex flex-col">

        <!-- Box 1 -->
        <div class="relative min-h-[400px] h-auto">
            <!-- Gradient -->
            <div class="absolute inset-0 w-full z-0 flex items-center bg-gradient-to-br from-primary-700 via-primary-500 to-primary-400">
            </div>

            <!-- Banner box -->
            <div class="relative z-1 flex items-center justify-center h-auto">
            
                <!-- Column -->
                <div class="w-full max-w-[1400px] px-[100px] py-[100px]">
                    <!-- Row -->
                    <div class="flex w-full justify-between gap-6">
                    
                        <!-- Column -->
                        <div class="flex flex-col gap-6 max-w-xl">
                            <p class="text-6xl font-bold text-white">
                                ¿No te da la pensión para tus hijos?
                            </p>
                            <p class="text-4xl font-semibold text-white">
                                ¡Obtén una orden de descuento judicial en menos de 48 horas!
                            </p>
                        </div>
                
                        <!-- Image -->
                        <img
                            src="images/home_page_img.png"
                            alt="Padres discutiendo"
                            class="h-90 object-contain"
                        />
                    </div>
                </div>
            </div>
        </div>

        <!-- Box 2 -->
        <div class="py-16">
            <div class="w-[300px] h-[300px] flex flex-col">
                ...
            </div>
        </div>
    </div>
</main>

<footer>
    <Footer/>
</footer>




<style>
</style>