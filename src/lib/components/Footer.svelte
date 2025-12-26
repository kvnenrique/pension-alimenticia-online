<script lang="ts">
    import { DarkMode } from "flowbite-svelte";
    import { STRINGS } from "$lib/strings";
    import { Footer, FooterCopyright, FooterLinkGroup, FooterLink, FooterBrand, FooterIcon } from "flowbite-svelte";
    import { FacebookSolid, XSolid } from "flowbite-svelte-icons";
</script>
  
<Footer footerType="socialmedia" class="dark dark:bg-4T">
    <div class="md:flex md:justify-between">
        <div class="mb-6 md:mb-0">
            <!-- 
                FooterBrand:
                src="/images/flowbite-svelte-icon-logo.svg" 
             -->    
            <FooterBrand
                href="/" 
                alt="Flowbite Logo" 
                name="{STRINGS.appName}"
            />
        </div>
        <div class="grid grid-cols-2 gap-8 sm:grid-cols-3 sm:gap-6">
            <!--
            <div>
                <h2 class="mb-6 text-sm font-semibold text-gray-900 uppercase dark:text-white">Resources</h2>
                <FooterLinkGroup>
                    <FooterLink class="mb-4" href="/">Flowbite</FooterLink>
                    <FooterLink class="mb-4" href="/">Tailwind CSS</FooterLink>
                </FooterLinkGroup>
            </div>
            --> 
            <div>
                <h2 class="mb-6 text-sm font-semibold text-gray-900 uppercase dark:text-white">{STRINGS.follow_us}</h2>
                <FooterLinkGroup>
                    <FooterLink class="mb-4" href="/">Facebook</FooterLink>
                    <FooterLink class="mb-4" href="/">X</FooterLink>
                </FooterLinkGroup>
            </div>
            <div>
                <h2 class="mb-6 text-sm font-semibold text-gray-900 uppercase dark:text-white">{STRINGS.legal}</h2>
                <FooterLinkGroup>
                    <FooterLink class="mb-4" href="/privacy_policy">{STRINGS.privacy_policy}</FooterLink>
                    <FooterLink class="mb-4" href="/terms_and_conditions">{STRINGS.terms_and_conditions}</FooterLink>
                </FooterLinkGroup>
            </div>
        </div>
    </div>

    <hr class="my-6 border-gray-200 sm:mx-auto lg:my-8 dark:border-gray-500" />
    
    <!-- Icons -->
    <div class="sm:flex sm:items-center sm:justify-between">
        <!-- Copy rights-->
        <FooterCopyright href="/" by="{STRINGS.appName}™" />
        <!-- Icons-->
        <div class="mt-4 flex space-x-6 sm:mt-0 sm:justify-center rtl:space-x-reverse">
            <FooterIcon href="/">
                <FacebookSolid class="h-5 w-5 text-gray-500 hover:text-gray-900 dark:text-gray-500 dark:hover:text-white" />
            </FooterIcon>
            <FooterIcon href="/">
                <XSolid class="h-5 w-5 text-gray-500 hover:text-gray-900 dark:text-gray-500 dark:hover:text-white" />
            </FooterIcon>
        </div>
    </div>
</Footer>