<script setup lang='ts'>

</script>
<template>
    <Head>
        <Title>Blog</Title>
    </Head>
    <Header url="blog"></Header>
    <OtherLanding name="Blog"></OtherLanding>
    <Blog></Blog>
    <Review></Review>
    <Contact></Contact>
    <Footer></Footer>
</template>
<style scoped>
.blog p.middle {
    text-align: center;
    max-width: 1000px;
    margin: auto;
    margin-bottom: 2rem;
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