<script>
    import { Input, Label, Helper, Textarea, Button, Checkbox, A, FooterIcon, StepIndicator} from "flowbite-svelte" 
    import { FacebookSolid, XSolid } from "flowbite-svelte-icons";
    import { STRINGS } from "$lib/strings";
    import { CONTACT } from "$lib/values";
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
                        <h2 class="text-2xl">{STRINGS.headquarters_and_offices}</h2>
                        <p>
                             {CONTACT.address}
                        </p>
                    </div>
                    <br>
                    <!-- Contact data -->
                    <div>
                        <h2 class="text-2xl">{STRINGS.contact}</h2>
                        <p>
                            <b>{STRINGS.phone}</b>: {CONTACT.phone}
                        </p>
                        <p>
                            <b>{STRINGS.email}</b>: {CONTACT.email}
                        </p>
                    </div>
                    <br>
                    <!-- Social networks -->
                    <div>
                        <h2 class="text-2xl">{STRINGS.follow_us}</h2>
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
                                <Label>{STRINGS.name}</Label>
                                <Input placeholder="{STRINGS.name}"/>
                            </div>
                            <div>
                                <Label>{STRINGS.email}</Label>
                                <Input placeholder="ejemplo@gmail.com"/>
                            </div>
                            <div>
                                <Label>{STRINGS.subject}</Label>
                                <Input placeholder="{STRINGS.subject}"/>
                            </div>
                            <div>
                                <Label>{STRINGS.message}:</Label>
                                <Textarea
                                    rows={10}
                                    class="w-full"
                                />
                            </div>
                            <Checkbox classes={{ div: "mb-6 gap-1 rtl:space-x-reverse" }} required>
                                {STRINGS.i_have_read_and_agreed_} <A href="/" class="text-primary-700 dark:text-primary-600 hover:underline">{STRINGS.terms_and_conditions}</A>.
                            </Checkbox>
                            <!-- Send button -->
                            <div>
                                <Button type="submit">
                                    {STRINGS.submit}
                                </Button>
                            </div>
                        </div>
                    </form>
                </div>
             </div>
         </div>
    </div>
</div>
