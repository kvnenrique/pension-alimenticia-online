<script lang="ts">
    import { STRINGS } from "$lib/strings";
    import { Input, Label, Button, Textarea, Fileupload, Helper, Checkbox, A } from 'flowbite-svelte';

    let selectedFiles = $state<FileList | null>(null);
    let fileNames = $derived(
        selectedFiles
        ? Array.from(selectedFiles)
            .map((file) => file.name)
            .join(", ")
        : "No files selected"
    );
    let curp = $state('')

    //
    // Functions
    //

    /*
     * Handler for CURP input, allows only uppercase letters and numbers
     * and constraints the length of the string to 18 characters.
     * @param e
     **/
    function handleCurpInput(e) {
        curp = e.target.value
            .toUpperCase()
            .replace(/[^A-Z0-9]/g, '')
            .slice(0, 18)

        e.target.value = curp
    }
</script>



<!--
  bg-red-500
-->
<div class="text-justify">
    <!-- Title -->
     <h1 class="text-4xl font-semibold">{STRINGS.registration_form}</h1>

    <div class="mx-auto max-w-3xl">
        <form>
            <!-- 
                Marritage certificate 
            -->
            <section>
                <hr class="my-6 border-gray-700 sm:mx-auto lg:my-8 dark:border-gray-700" />
                <h2 class="text-2xl">{STRINGS.marritage_certificate}</h2>
                <br>
                <div>
                    <label>
                        {STRINGS.marritage_certificate}
                        <Fileupload class="mb-2"/>
                        <Helper>PDF, PNG or JPG</Helper>
                    </label>
                </div>
            </section>


            <!-- 
                Minor's data
            -->
            <section>
                <hr class="my-6 border-gray-700 sm:mx-auto lg:my-8 dark:border-gray-700" />
                <h2 class="text-2xl">{STRINGS.data_of_minors}</h2>
                <br>
                
                <label>
                    {STRINGS.birth_certificate_of_minors}
                    <Fileupload clearable bind:files={selectedFiles} multiple />
                    <Helper color="emerald" class="mt-2">Selected files: {fileNames}</Helper>
                </label>
            </section>


            <!-- 
                Debtor's data 
            -->
            <section>
                <hr class="my-6 border-gray-700 sm:mx-auto lg:my-8 dark:border-gray-700" />
                <h2 class="text-2xl">{STRINGS.debtors_data}</h2>
                <br>
                <!-- RFC -->
                <div>
                    <Label>{STRINGS.rfc}</Label>
                    <Input placeholder={STRINGS.rfc}/>
                </div>
                <!-- CURP -->
                <div>
                    <Label>{STRINGS.curp}</Label>
                    <Input 
                        placeholder={STRINGS.curp} 
                        bind:value={curp} 
                        oninput={handleCurpInput}
                        />
                </div>
                <br>
                <div>
                    <Label>
                        {STRINGS.payslip}
                        <Fileupload class="mb-2"/>
                        <Helper>PDF, PNG or JPG.</Helper>
                    </Label>
                </div>
            </section>
            

            <!-- 
                Explanation of the situation 
            -->
            <section>
                <hr class="my-6 border-gray-700 sm:mx-auto lg:my-8 dark:border-gray-700" />
                <h2 class="text-2xl">{STRINGS.explanation_of_the_situation}</h2>
                <br>
                <p>
                    Escriba un breve relato de la situación que responda las siguientes preguntas:
                </p>
                <ul class="list-disc ml-8">
                    <li>¿Cuál es el nombre completo del demandado?</li>
                    <li>¿Dónde trabaja actualmente?</li>
                    <li>¿Qué puesto desempeña u oficio tiene?</li>
                    <li>¿Existe parentesco legal con el menor?</li>
                </ul>
                <br>

                <!--
                    class="focus:ring-primary-500 focus:border-primary-500"
                -->
                <Textarea
                    rows={10}
                    class="block w-full rounded-lg border border-gray-300 p-2.5 text-sm"
                />
            </section>


            <!-- 
                Terms and conditions 
            -->
            <section>
                <hr class="my-6 border-gray-700 sm:mx-auto lg:my-8 dark:border-gray-700" />
                <h2 class="text-2xl">{STRINGS.terms_and_conditions}</h2>
                <br>
                <Checkbox classes={{ div: "mb-6 gap-1 rtl:space-x-reverse" }} required>
                    {STRINGS.i_have_read_and_agreed_} 
                    <A href="/terms_and_conditions" class="dark:text-primary-600 hyperlink">{STRINGS.terms_and_conditions}</A>
                    {STRINGS.and}
                    <A href="/privacy_policy" class="dark:text-primary-600 hyperlink">{STRINGS.privacy_policy}</A>.
                </Checkbox>
            </section>

            <!-- 
                Submit button 
            -->
            <div class="pt-4 text-center">
                <Button type="submit">
                    {STRINGS.submit}
                </Button>
            </div>
        </form>
    </div>
</div>