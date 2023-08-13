<script setup lang='ts'>
</script>
<template>
    <section class="contact">
        <div class="page">
            <form>
                <img class="small" src="../public/images/lab.jpg" alt="lab">
                <div class="content">
                    <h2>Get in <span>Touch.</span></h2>
                    <div class="col-2">
                        <input type="text" placeholder="First Name">
                        <input type="text" placeholder="Last Name">
                    </div>
                    <div class="col-2">
                        <input type="text" placeholder="Phone">
                        <input type="email" placeholder="Email">
                    </div>
                    <textarea rows="6" placeholder="Comment"></textarea>
                    <ArrowButton text="Submit"></ArrowButton>
                </div>
                <img class="big" src="../public/images/lab.jpg" alt="lab">
            </form>
        </div>
    </section>
</template>
<style scoped>
.contact {
    margin: 4rem 0;
}

.contact h2 {
    margin: 0.5em 0;
}

.contact h2 span {
    font-size: inherit;
    color: var(--color-primary);
}

.contact form {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 0.5rem;
    box-shadow: 0px 0px 40px 0px rgba(0, 0, 0, 0.08);
    min-height: 400px;
    align-items: center;
    background-color: white;
    border-radius: 12px;
}

.contact form .content {
    padding: 1.5rem;
}


.contact .col-2 {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 0.8rem;
    margin-bottom: 0.8rem;
}

.contact input,
.contact textarea {
    font-size: var(--medium-font);
    border: none;
    outline: none;
    border: 1px solid rgb(212, 212, 212);
    border-radius: 4px;
    padding: 0.8em 1em;
    width: 100%;
    resize: none;
}

.contact button {
    margin-top: 1rem;
}


/* -------------right ------------- */
.contact img {
    height: 100%;
    object-fit: cover;
    width: 100%;
    border-top-right-radius: 12px;
    border-bottom-right-radius: 12px;
}

.contact img.small {
    display: none;
}


@media only screen and (max-width: 900px) {
    .contact .col-2 {
        display: grid;
        grid-template-columns: 100%;
        gap: 0.8rem;
        margin-bottom: 0.8rem;
    }
}

@media only screen and (max-width: 700px) {
    .contact form {
        display: grid;
        grid-template-columns: 100%;
        gap: 0.5rem;
        box-shadow: 0px 0px 40px 0px rgba(0, 0, 0, 0.08);
        min-height: 400px;
        align-items: center;
        border-radius: 12px;
    }

    .contact img.small {
        display: block;
    }

    .contact img.big {
        display: none;
    }

    .contact img {
        border-radius: 12px 12px 0 0;
    }

    .contact button{
        width: 100%;
    }
}
</style>