<script>
    import Header from '../components/Header.svelte';
    import Footer from '../components/Footer.svelte'
    import { MaterialApp } from 'svelte-materialify';
</script>

<MaterialApp>
    <Header/>

    <slot/>

    <Footer/>
</MaterialApp>

