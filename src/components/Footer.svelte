<script>
    import { Footer } from 'svelte-materialify';
    import Icon from 'svelte-awesome';
    import { building, flask, phone, envelope  } from 'svelte-awesome/icons';
</script>

<style>

    .container {
        text-align: center;
        display: block;
    }

    .footer-info {
        color: white;
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 15px;
        padding: 3px;
    }

    span {
        padding-left: 5px;
    }
</style>

<Footer class="indigo justify-center pa-4">
    <div class="container">
        <div class="footer-info">
            <Icon data={phone}/>
            <span>+853 8822 4992</span>
        </div>
        <a href="mailto:echeung@um.edu.mo"><div class="footer-info">
            <Icon data={envelope}/>
            <span>echeung@um.edu.mo</span>
        </div></a>
        <div class="footer-info">
            <Icon data={building}/>
            <span>E12-4014</span>
            <span> / </span>
            <Icon data={flask}/>
            <span>N22-4001</span>
        </div>
        <div class="footer-info">
            <span>Faculty of Health Science</span>
        </div>
        <div class="footer-info">
            <span>University of Macau</span>
        </div>
    </div>



</Footer>
