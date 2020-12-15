<script>
    import Header from '../components/Header.svelte';
    import Footer from '../components/Footer.svelte'
    import { MaterialApp, Row, Col } from 'svelte-materialify';
</script>

<style global>
    @import url('https://fonts.googleapis.com/css2?family=Raleway');

    body {
        color: #777777;
        background: #f7f7f7;
        font-family: 'Raleway', sans-serif; /*-apple-system, BlinkMacSystemFont, Roboto, Oxygen-Sans, Ubuntu, Cantarell, "Helvetica Neue", sans-serif;*/
    }

</style>

<MaterialApp>
    <Header/>

    <slot/>

    <Footer/>
</MaterialApp>

