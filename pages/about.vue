<script setup lang='ts'>

</script>
<template>
    <Head>
        <Title>About</Title>
    </Head>
    <Header url="about"></Header>
    <OtherLanding name="About"></OtherLanding>
    <About></About>
    <section class="slogan">
        <div class="page">
            <div>
                <h2>Our Vision</h2>
                <p>Commitment towards patient Care, Cure & Quality Health. Commitment towards patient Care, Cure & Quality
                    Health.
                </p>
            </div>
            <span class="line"></span>
            <div>
                <h2>Our Mission</h2>
                <p>To become leading health system with high end Infrastructure, Instruments & Professionals.</p>
            </div>
        </div>
    </section>
    <Team></Team>
    <Contact></Contact>
    <Footer></Footer>
</template>
<style scoped>
.slogan {
    background-color: #F6FAFF;
}

.slogan .page {
    display: grid;
    grid-template-columns: 1fr max-content 1fr;
    gap: 3rem;
    align-items: center;
    padding: 2rem;
}

.slogan h2 {
    margin: 0;
    color: var(--color-primary);
}


.slogan .line {
    width: 1px;
    display: block;
    height: 100%;
    background-color: #e2e2e2;
}

@media only screen and (max-width: 800px) {
    .slogan .page {
        grid-template-columns: 100%;
        gap: 2rem;
    }

    .slogan .line {
        display: none;
    }
}
</style>