<script setup lang='ts'>

</script>
<template>
    <Head>
        <Title>Appointment</Title>
    </Head>
    <Header url="appointment"></Header>
    <OtherLanding name="Book Appointment"></OtherLanding>
    <section class="appoint">
        <div class="page">
            <div class="left">
                <h2><span>Book You Slot Now</span> And Save Your Time </h2>
                <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the
                    industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and
                    scrambled it to make a type specimen book.</p>
            </div>
            <div class="right">
                <form>
                    <h2>Book Appointment</h2>
                    <input type="text" placeholder="First Name">
                    <input type="text" placeholder="Phone Number">
                    <input type="text" placeholder="Email">
                    <input type="text" placeholder="Appointment Date">
                    <input type="text" placeholder="Appointment Time">
                    <input type="text" placeholder="Location">
                    <ArrowButton text="Book Appointment"></ArrowButton>
                </form>
            </div>
        </div>
        <img src="../public/images/outlines/flower-outline.png">
    </section>
    <Footer></Footer>
</template>
<style scoped>
.appoint button {
    width: 100%;
    margin-top: 1rem;
}

.appoint {
    margin-top: 3rem;
    position: relative;
    min-height: 400px;
}

.appoint img {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 400px;
    z-index: -1;
}

.appoint .page {
    display: grid;
    grid-template-columns: 1fr 1.2fr;
    padding-top: 3rem;
    gap: 2rem;
}

.appoint .page h2 span {
    font-size: inherit;
    color: var(--color-primary);
}


.appoint form {
    width: 100%;
    background-color: white !important;
    padding: 2rem;
    box-shadow: 0px 0px 40px 0px rgba(0, 0, 0, 0.1);
    border-radius: 12px;
}

.appoint form h2 {
    margin-top: 0;
}


.appoint input {
    font-size: var(--medium-font);
    border: none;
    outline: none;
    border: 1px solid rgb(212, 212, 212);
    border-radius: 4px;
    padding: 0.8em 1em;
    width: 100%;
    resize: none;
    margin-bottom: 1rem;
}





@media only screen and (max-width: 700px) {
    .appoint .page {
        grid-template-columns: 100%;
    }
}
</style>