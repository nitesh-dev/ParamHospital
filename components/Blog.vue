<script setup lang='ts'>
import blog1 from '~/public/images/blog/blog1.jpg'
import blog2 from '~/public/images/blog/blog2.jpg'
import blog3 from '~/public/images/blog/blog3.jpg'

const data = Array<{
    title: string,
    date: string,
    text: string,
    url: string,
    image: string
}>()

data.push({
    title: 'From its medieval origins to the digital era everything',
    date: '12 jul 2023',
    text: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry\'s. ',
    url: '#',
    image: blog1
})

data.push({
    title: 'Mukhyamantri Amrutum - An Initiative of health',
    date: '12 jul 2023',
    text: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry\'s. ',
    url: '#',
    image: blog2
})

data.push({
    title: 'From its medieval origins to the digital era everything',
    date: '12 jul 2023',
    text: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry\'s. ',
    url: '#',
    image: blog3
})

data.push({
    title: 'From its medieval origins to the digital era everything',
    date: '12 jul 2023',
    text: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry\'s. ',
    url: '#',
    image: blog1
})

data.push({
    title: 'Mukhyamantri Amrutum - An Initiative of health',
    date: '12 jul 2023',
    text: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry\'s. ',
    url: '#',
    image: blog2
})

</script>
<template>
    <section class="blog">
        <div class="page">
            <div class="left">
                <h5>Blogs and News</h5>
                <h2>Blog and News</h2>
                <p>Lorem Ipsum is not simply random text. It has roots in a piece of classical Latin literature from 45 BC,
                    making it over 2000 years old. Richard McClintock, a Latin professor at Hampden-Sydney. Lorem Ipsum is
                    not simply random text. It has roots in a piece of classical Latin literature from 45 BC, making it over
                    2000 years old. Richard McClintock, a Latin professor at Hampden.
                </p>
                <ArrowButton text="View More"></ArrowButton>
            </div>
            <div class="right container hide-scroll">
                <div v-for="item in data" class="card">
                    <div>
                        <div class="image-holder">
                            <img :src="item.image">
                            <span class="label">{{ item.date }}</span>
                        </div>
                        <div class="content">
                            <h4>{{ item.title }}</h4>
                            <p>{{ item.text }}</p>
                            <a :href="item.url">Read More &#8594;</a>
                        </div>
                        <img class="health" src="../public/images/outlines/health.png" alt="health">
                    </div>
                </div>
            </div>

        </div>
    </section>
</template>
<style scoped>

.blog{
    margin: 3rem 0;
}
.blog .page {
    display: grid;
    grid-template-columns: 1fr 2fr;
}


/* ----------------- left -------------- */
.blog .left h5 {
    margin: 0;
    color: var(--color-primary);
}

.blog .left h2 {
    margin-top: 0.5rem;
}

.blog .left button {
    margin-top: 1.5rem;
}



/* ----------------- right --------------- */
.blog .right {
    display: flex;
}


.blog .container {
    display: flex;
    overflow: auto;
}

.blog .card {
    min-width: 300px;
    width: 300px;
}

.blog .card>div {
    border-radius: 8px;
    margin: 1rem 0.5rem;
    box-shadow: 0px 0px 40px 0px rgba(0, 0, 0, 0.06);
    position: relative;
}

.blog .card .image-holder img {
    border-radius: 8px 8px 0 0;
    width: 100%;
    height: 170px;
    object-fit: cover;

}

.blog .content {
    padding: 1rem;
}

.blog .content h4 {
    margin: 0;
    color: var(--color-primary);
}

.blog .content a {
    color: var(--color-primary);
    font-weight: bold;
}

.blog .image-holder{
    position: relative;
    display: flex;
}

.blog .label{
    position: absolute;
    bottom: 0;
    left: 0;
    background-color: var(--color-primary);
    color: white;
    padding: 0.5em 1em;
    font-size: var(--small-font);
    border-radius: 12px 12px 0 0;
}

.blog .health{
    width: 50px;
    height: auto;
    position: absolute;
    right: 0.4rem;
    bottom: 0.5rem;
}
</style>