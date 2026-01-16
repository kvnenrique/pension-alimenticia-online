
<script>
    import Navbar from '$lib/components/Navbar.svelte'
    import Footer from '$lib/components/Footer.svelte'
    import { Card, Button }  from 'flowbite-svelte'
    import { STRINGS } from '$lib/strings';
</script>




<header>
    <Navbar/>
</header>
<main>
    <!-- Column -->
    <div class="bg-zinc-100 flex flex-col">

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
        <div class="w-screen flex justify-center">
            <!-- Main col -->
            <div class="flex flex-col items-center w-full max-w-[1400px] px-[100px] py-[100px]">
                <Card size="xl" class="self-stretch w-full py-12 px-4 text-center">
                    <h5 class="mb-2 text-4xl font-semibold text-gray-900 dark:text-white">Iniciar procedimento en línea</h5>
                    <!-- <p class="mb-5 text-base text-gray-500 sm:text-lg dark:text-gray-400">Stay up to date and move work forward with Flowbite on iOS & Android. Download the app today.</p> -->
                    <br>
                    <br>
                    <div class="items-center justify-center space-y-4 sm:flex sm:space-y-0 sm:space-x-4 rtl:space-x-reverse">
                        <Button
                            size="xl"
                            class="inline-flex w-fit"
                            href="/request_form"
                        >
                            {STRINGS.start_procedure}
                        </Button>
                    </div>
                </Card>
            </div>
        </div>
    </div>
</main>

<footer>
    <Footer/>
</footer>




<style>
</style>