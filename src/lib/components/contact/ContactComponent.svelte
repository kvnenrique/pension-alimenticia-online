<script>
    import { Input, Label, Helper, Textarea, Button, Checkbox, A } from "flowbite-svelte" 
    import { STRINGS } from "$lib/strings";
</script>

<div class="text-justify bg-secondary-200 w-full">
    <!-- Title -->
    <h1 class="text-4xl font-semibold">{STRINGS.contact_us}</h1>
    <br>

    <div class="relative z-1 flex items-center justify-center h-auto w-full">
        <!-- Column -->
         <div class="w-full max-w-[1400px] py-[50px] bg-amber-200">
            <!-- Row -->
             <div class="flex w-full justify-between gap-6">
                <!-- data column -->
                <div class="w-full flex col gap-6 bg-pink-400" style="height: 100px;">

                </div>

                <!-- Email column -->
                <div class="w-full flex flex-col bg-pink-300">
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
