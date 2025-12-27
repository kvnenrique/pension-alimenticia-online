<script>
    import { STRINGS } from "$lib/strings";
    import { Input, Label, Button, Textarea } from 'flowbite-svelte';
</script>




<div class="text-justify bg-red-500">
    <!-- Title -->
     <h1 class="text-4xl">{STRINGS.registration_form}</h1>

    <div class="mx-auto max-w-3xl">
        <form>
            <!-- Marritage certificate -->
            <section>
                <hr class="my-6 border-gray-700 sm:mx-auto lg:my-8 dark:border-gray-700" />
                <h2 class="text-2xl">{STRINGS.marritage_certificate}</h2>
                <div>
                    <label>
                        {STRINGS.marritage_certificate}
                        <Button>{STRINGS.choose_document}</Button>
                    </label>
                </div>
            </section>


            <!-- Data of minors -->
            <section>
                <hr class="my-6 border-gray-700 sm:mx-auto lg:my-8 dark:border-gray-700" />
                <h2 class="text-2xl">{STRINGS.data_of_minors}</h2>
            </section>


            <!-- Debtors data -->
            <section>
                <hr class="my-6 border-gray-700 sm:mx-auto lg:my-8 dark:border-gray-700" />
                <h2 class="text-2xl">{STRINGS.debtors_data}</h2>
                <div>
                    <Label>{STRINGS.rfc}</Label>
                    <Input placeholder={STRINGS.rfc}/>
                </div>
                <div>
                    <Label>{STRINGS.curp}</Label>
                    <Input placeholder={STRINGS.curp}/>
                </div>
                <div>
                    <Label>
                        {STRINGS.payslip}
                        <Button>{STRINGS.choose_document}</Button>
                    </Label>
                </div>
            </section>
            

            <!-- Explanation of the situation -->
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
                <Textarea
                    rows={10}
                    class="block w-full rounded-lg border border-gray-300 p-2.5 text-sm
                        focus:ring-primary-500 focus:border-primary-500"
                />
            </section>


            <!-- Terms and conditions -->
            <section>
                <hr class="my-6 border-gray-700 sm:mx-auto lg:my-8 dark:border-gray-700" />
                <h2 class="text-2xl">{STRINGS.terms_and_conditions}</h2>
                <br>
                <label>
                    <input type="checkbox" checked={false}/>
                    {STRINGS.i_have_read_and_agreed_} 
                    <a class="text-blue-600 underline"  href="/terms_and_conditions">
                        {STRINGS.terms_and_conditions}
                    </a>
                    {STRINGS.and}
                    <a class="text-blue-600 underline" href="/privacy_policy">
                        {STRINGS.privacy_policy}
                    </a>
                </label>
            </section>

            <!-- Submit button -->
            <div class="pt-4 text-center">
                <Button color="green" size="lg">{STRINGS.submit}</Button>
            </div>
        </form>
    </div>
</div>