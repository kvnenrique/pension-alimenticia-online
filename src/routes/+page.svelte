
<script>
    import Navbar from '$lib/components/Navbar.svelte'
    import Footer from '$lib/components/Footer.svelte'
</script>




<header>
    <Navbar/>
</header>
<main>
    <h1>Welcome to SvelteKit</h1>
    <p>Visit <a href="https://svelte.dev/docs/kit">svelte.dev/docs/kit</a> to read the documentation</p>

    <div class="myBox"></div>

    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Iure pariatur harum quibusdam ratione, culpa cum officia! Sint consectetur omnis, ratione dolorem sunt optio est ullam, quae officia tempore fugit. Quidem.</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Totam veritatis doloribus neque excepturi repellat iusto quidem. Labore, itaque voluptatibus sunt fugiat pariatur ut facilis minus, recusandae libero error repudiandae delectus.</p>

</main>
<footer>
    <Footer/>
</footer>




<style>
    .myBox {
        width: 300px;
        height: 300px;
    }
</style>