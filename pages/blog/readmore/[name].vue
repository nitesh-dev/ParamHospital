<script setup lang='ts'>

</script>
<template>
    <Head>
        <Title>Blog</Title>
    </Head>
    <Header url="blog"></Header>
    <OtherLanding name="Blog"></OtherLanding>
    <section class="blog">
        <div class="page">
            <h5>Blog and News</h5>
            <h2>Blog and News</h2>
            <p class="middle">Lorem Ipsum is not simply random text. It has roots in a piece of classical Latin literature
                from 45 BC, making it over 2000 years old. Richard McClintock, a Latin professor at Hampden-Sydney.Lorem
                Ipsum is not simply random text. It has roots in a piece of classical Latin literature from 45 BC, making it
                over 2000 years old. Richard McClintock, a Latin professor at Hampden.
            </p>
            <div class="news">
                <img src="../../../public/images/blog/news.png">
                <div class="content">
                    <h3>From its medieval origins to the digital era everything</h3>
                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut lobortis massa vitae ligula accumsan,
                        vitae pulvinar justo tincidunt. Mauris ornare ultrices sapien, in interdum turpis bibendum sed.
                        Fusce at dolor consequat, faucibus tortor sit amet, fermentum dui. Suspendisse vestibulum urna a
                        euismod auctor. Morbi convallis non ante vel vehicula. Aliquam malesuada hendrerit ipsum, et gravida
                        nunc posuere et. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus
                        mus. Phasellus et elementum quam, a elementum ex. Mauris non pellentesque nulla. Mauris in ultricies
                        ex. Proin at arcu et felis congue sollicitudin quis a urna. In fermentum dui sem.Phasellus eu
                        lacinia neque. Donec venenatis auctor augue accumsan feugiat. Vestibulum vel pharetra tellus. Duis
                        in leo ullamcorper, fringilla erat eget, ultricies risus. Sed ullamcorper mi non ultricies
                        pellentesque.
                    </p>

                    <p>Nullam lacinia ac orci nec porta. Pellentesque tristique lorem lacus, sit amet scelerisque eros
                        consequat non. Vestibulum ornare lacinia purus, eget gravida ante iaculis a. Quisque scelerisque
                        libero at neque pretium egestas. Ut accumsan sagittis sem, id maximus urna vestibulum ac. Sed a
                        nulla feugiat, molestie quam sed, venenatis arcu. Integer nec lacus tempor est varius aliquam. Donec
                        ac urna in turpis laoreet interdum at eu orci.
                    </p>

                    <p>Quisque scelerisque libero at neque pretium egestas. Ut accumsan sagittis sem, id maximus urna
                        vestibulum ac. Sed a nulla feugiat, molestie quam sed, venenatis arcu. Integer nec lacus tempor est
                        varius aliquam. Donec ac urna in turpis laoreet interdum at eu orci.
                    </p>
                </div>
            </div>
        </div>
    </section>
    <Contact></Contact>
    <Footer></Footer>
</template>
<style scoped>
.blog p.middle {
    text-align: center;
    max-width: 1260px;
    margin: auto;
    margin-bottom: 3rem;
}

.blog h5 {
    color: var(--color-primary);
    text-align: center;
    margin-bottom: 0.5em;
}

.blog button {
    margin: auto;
    margin-top: -1rem;
}

.blog h2 {
    margin-top: 0;
    text-align: center;
}

.blog .news {
    display: grid;
    grid-template-columns: 1fr 1.2fr;
    gap: 2rem;
}

.blog .news h3 {
    margin-top: 0;
    font-size: 35px;
}

.blog .news img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: 12px;
}


@media only screen and (max-width: 700px) {
    .blog .news {
        grid-template-columns: 100%;
    }
}
</style>