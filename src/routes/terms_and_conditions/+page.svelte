<script>
    import Navbar from '$lib/components/Navbar.svelte'
    import Footer from '$lib/components/Footer.svelte'
</script>




<header>
    <Navbar/>
</header>
<main>
    <div class="myBox">
        <p>Términos y condiciones</p>
    </div>
</main>
<footer>
    <Footer/>
</footer>




<style>
    .myBox {
        width: 300px;
        height: 300px;
        background-color: bisque;
    }
</style>