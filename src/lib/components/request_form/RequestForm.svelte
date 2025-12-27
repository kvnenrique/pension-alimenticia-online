
<script>
    import { STRINGS } from "$lib/strings";
    import { Input, Label, Button, Textarea } from 'flowbite-svelte';
</script>
<div class="text-justify">
    <!-- Title -->
     <h1 class="text-4xl">{STRINGS.registration_form}</h1>

    <div class="mx-auto max-w-3xl">
        <form class="bg-red-500">
            <!-- Marritage certificate -->
            <section>
                <hr class="my-6 border-gray-700 sm:mx-auto lg:my-8 dark:border-gray-700" />
                <h2 class="text-2xl">{STRINGS.marritage_certificate}</h2>
                <div>
                    <Label>{STRINGS.marritage_certificate}</Label>
                    <Button>{STRINGS.choose_document}</Button>
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
                    <Label>{STRINGS.payslip}</Label>
                    <Button>{STRINGS.choose_document}</Button>
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
        </form>
    </div>



      <div class="mx-auto max-w-3xl">
      
        <form class="space-y-6">
          <!-- Name -->
          <div>
            <Label class="mb-2 block">Name</Label>
      
            <div class="grid grid-cols-1 gap-4 md:grid-cols-2">
              <div>
                <Input placeholder="First Name" />
                <p class="mt-1 text-sm text-gray-500">First Name</p>
              </div>
      
              <div>
                <Input placeholder="Last Name" />
                <p class="mt-1 text-sm text-gray-500">Last Name</p>
              </div>
            </div>
          </div>
      
          <!-- Email -->
          <div>
            <Label>Email</Label>
            <Input type="email" placeholder="example@example.com" />
          </div>
      
          <!-- Title of document -->
          <div>
            <Label>Title of the document</Label>
            <Input />
          </div>
      
          <!-- Description -->
          <div>
            <Label>Description of the document</Label>
            <Textarea placeholder="Type here..." />
          </div>
      
          <!-- File upload -->
          <div>
            <Label>Please upload your document</Label>
      
            <!--<FileUpload
              dropzone
              class="mt-2"
              accept=".pdf,.doc,.docx"
            >
              <p class="text-sm text-gray-500">
                Drag and drop files here or click to browse
              </p>
            </FileUpload> -->
          </div>
      
          <!-- Submit -->
          <div class="pt-4 text-center">
            <Button color="green" size="lg">
              Submit
            </Button>
          </div>
        </form>
      </div>
      
</div>