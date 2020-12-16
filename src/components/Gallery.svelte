<script>
    export let items;
    import Slidy from 'svelte-slidy';
    const slidy = {
        slides: items,
        wrap: {
            id: 'slidy_cards',
            width: '100%',
            height: '50vh',
            padding: '0',
        },
        slide: {
            gap: 0,
            width: '100vw',
            height: '100vh',
            backimg: false,
        },
        controls: {
            dots: true,
            dotsnum: false,
            dotsarrow: true,
            dotspure: true,
            arrows: false,
            keys: true,
            drag: true,
            wheel: true,
        },
        duration: 350,
        axis: 'x'
    }
</script>

<style>
@media screen and (min-width: 500px) {
    :global(#slidy_cards .slidy-ul li) {width: 70%;}
}
@media screen and (min-width: 600px) {
    :global(#slidy_cards .slidy-ul li) {width: 50%;}
}
@media screen and (min-width: 700px) {
    :global(#slidy_cards .slidy-ul li) {width: 33%;}
}

:global(#slidy_cards) {
    color: mediumpurple;
}

:global(#slidy_cards button) {
    color: #3F51B5;
}

:global(#slidy_cards .slidy-dots li.active button) {
    background: #3F51B5;
    transform: scale(1.3);
}

:global(#slidy_cards .slidy-ul li img) {
    height: 80%;
    transform: scale(1);
    transition: transform 350ms, box-shadow 350ms;
}
:global(#slidy_cards .slidy-ul li.active img) {
    transform: scale(1.15);
    box-shadow: 0 14px 25px rgba(0, 0, 0, 0.36);
}
.slide {
    position: relative;
    display: flex;
    flex-flow: column;
    text-align: center;
    align-content: center;
    justify-content: center;
    height: 100%;
    border-radius: 1rem;
}
.slide img {
    max-height: 300px;
    width: auto;
    height: 100%;
    box-sizing: border-box;
    vertical-align: middle;
    object-fit: cover;
    position: relative;
    z-index: 1;
    border-radius: 1rem;
    box-shadow: 0 14px 25px rgba(0, 0, 0, 0.16);
}
.slide article {
    margin-top: 20px;
    padding: 20px;
}

</style>

<Slidy {...slidy} let:item >
    <div class="slide">
        <img alt="{item.header}" src="{item.src}"/>
        <article>
            <p style="color: #333;">
                {item.text}
            </p>
        </article>
    </div>
</Slidy>