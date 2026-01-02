<script>
    import { Input, Label, Helper, Textarea, Button, Checkbox, A, FooterIcon} from "flowbite-svelte" 
    import { FacebookSolid, XSolid } from "flowbite-svelte-icons";
    import { STRINGS } from "$lib/strings";
</script>

<div class="text-justify w-full">
    <!-- Title -->
    <h1 class="text-4xl font-semibold">{STRINGS.contact_us}</h1>
    <br>

    <div class="relative z-1 flex items-center justify-center h-auto w-full">
        <!-- Column -->
         <div class="w-full max-w-[1400px] py-[50px]">
            <!-- Row -->
             <div class="flex w-full justify-between gap-12">
                <!-- data column -->
                <div class="w-full flex-col gap-6">
                    <!-- Address -->
                    <div>
                        <h2 class="text-2xl">Sede central y oficinas</h2>
                        <p>
                             Camino del Charcazo S/N 1456, San Lorenzo de la Parrilla, Toluca, Estado de México.
                        </p>
                    </div>
                    <br>
                    <!-- Contact data -->
                    <div>
                        <h2 class="text-2xl">Contacto</h2>
                        <p>
                            <b>Teléfono</b>: 345-345-144
                        </p>
                        <p>
                            <b>Email</b>: contacto@alejando.abogados.com
                        </p>
                    </div>
                    <br>
                    <!-- Social networks -->
                    <div>
                        <h2 class="text-2xl">Síguenos</h2>
                        <div class="w-full flex flex-row gap-6">
                            <A href="/">
                                <FacebookSolid class="h-5 w-5 text-gray-500 hover:text-gray-900 dark:text-gray-500 dark:hover:text-white" />
                            </A>
                            <A href="/">
                                <XSolid class="h-5 w-5 text-gray-500 hover:text-gray-900 dark:text-gray-500 dark:hover:text-white" />
                            </A>
                        </div>
                    </div>
                </div>

                <!-- Email column -->
                <div class="w-full flex flex-col">
                    <form>
                        <!-- Column -->
                        <div class="flex flex-col gap-3">
                            <div>
                                <Label>Nombre</Label>
                                <Input placeholder="Nombre"/>
                            </div>
                            <div>
                                <Label>Correo electrónico</Label>
                                <Input placeholder="ejemplo@gmail.com"/>
                            </div>
                            <div>
                                <Label>Asunto</Label>
                                <Input placeholder="Asunto"/>
                            </div>
                            <div>
                                <Label>Mensaje:</Label>
                                <Textarea
                                    rows={10}
                                    class="w-full"
                                />
                            </div>
                            <Checkbox classes={{ div: "mb-6 gap-1 rtl:space-x-reverse" }} required>
                                I agree with the <A href="/" class="text-primary-700 dark:text-primary-600 hover:underline">terms and conditions</A>.
                            </Checkbox>
                            <!-- Send button row -->
                            <div>
                                <Button type="submit">
                                    Submit
                                </Button>
                            </div>
                        </div>
                    </form>
                </div>
             </div>
         </div>
    </div>
</div>
