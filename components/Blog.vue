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

        <div class="icons-button">

            <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 18 18" fill="none">
                <path fill-rule="evenodd" clip-rule="evenodd"
                    d="M12.4626 5.53814C12.5506 5.62625 12.6 5.74569 12.6 5.87022C12.6 5.99475 12.5506 6.11419 12.4626 6.20231L9.66432 9.00309L12.4633 11.8039C12.5488 11.8926 12.596 12.0113 12.5949 12.1345C12.5938 12.2577 12.5443 12.3756 12.4572 12.4626C12.3701 12.5497 12.2523 12.5991 12.1292 12.6001C12.006 12.6011 11.8874 12.5537 11.7989 12.4681L8.6681 9.33518C8.58016 9.24707 8.53076 9.12763 8.53076 9.00309C8.53076 8.87856 8.58016 8.75912 8.6681 8.67101L11.7989 5.53814C11.8425 5.49447 11.8943 5.45983 11.9513 5.43619C12.0083 5.41256 12.0694 5.40039 12.1311 5.40039C12.1928 5.40039 12.2539 5.41256 12.3109 5.43619C12.3679 5.45983 12.4196 5.49447 12.4633 5.53814H12.4626Z"
                    fill="#143584" />
                <path fill-rule="evenodd" clip-rule="evenodd"
                    d="M9.33177 5.53814C9.41971 5.62625 9.46911 5.74569 9.46911 5.87022C9.46911 5.99475 9.41971 6.11419 9.33177 6.20231L6.53346 9.00309L9.33239 11.8039C9.4179 11.8926 9.46518 12.0113 9.46405 12.1345C9.46292 12.2577 9.41348 12.3756 9.32636 12.4626C9.23925 12.5497 9.12144 12.5991 8.99831 12.6001C8.87517 12.6011 8.75657 12.5537 8.66804 12.4681L5.53724 9.33518C5.4493 9.24707 5.3999 9.12763 5.3999 9.00309C5.3999 8.87856 5.4493 8.75912 5.53724 8.67101L8.66804 5.53814C8.71165 5.49447 8.76343 5.45983 8.82043 5.43619C8.87743 5.41256 8.93852 5.40039 9.00022 5.40039C9.06191 5.40039 9.123 5.41256 9.18 5.43619C9.237 5.45983 9.28878 5.49447 9.33239 5.53814H9.33177Z"
                    fill="#143584" />
                <rect x="0.5" y="0.5" width="17" height="17" stroke="#143584" />
            </svg>

            <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 18 18" fill="none">
                <path fill-rule="evenodd" clip-rule="evenodd"
                    d="M5.53737 5.53814C5.44943 5.62625 5.40003 5.74569 5.40003 5.87022C5.40003 5.99475 5.44943 6.11419 5.53737 6.20231L8.33568 9.00309L5.53675 11.8039C5.45124 11.8926 5.40396 12.0113 5.40509 12.1345C5.40622 12.2577 5.45566 12.3756 5.54278 12.4626C5.62989 12.5497 5.7477 12.5991 5.87083 12.6001C5.99397 12.6011 6.11257 12.5537 6.2011 12.4681L9.3319 9.33518C9.41984 9.24707 9.46924 9.12763 9.46924 9.00309C9.46924 8.87856 9.41984 8.75912 9.3319 8.67101L6.2011 5.53814C6.15749 5.49447 6.10571 5.45983 6.04871 5.43619C5.99171 5.41256 5.93062 5.40039 5.86892 5.40039C5.80723 5.40039 5.74614 5.41256 5.68914 5.43619C5.63214 5.45983 5.58036 5.49447 5.53675 5.53814H5.53737Z"
                    fill="#143584" />
                <path fill-rule="evenodd" clip-rule="evenodd"
                    d="M8.66823 5.53814C8.58029 5.62625 8.53089 5.74569 8.53089 5.87022C8.53089 5.99475 8.58029 6.11419 8.66823 6.20231L11.4665 9.00309L8.66761 11.8039C8.5821 11.8926 8.53482 12.0113 8.53595 12.1345C8.53708 12.2577 8.58652 12.3756 8.67364 12.4626C8.76075 12.5497 8.87856 12.5991 9.00169 12.6001C9.12483 12.6011 9.24343 12.5537 9.33196 12.4681L12.4628 9.33518C12.5507 9.24707 12.6001 9.12763 12.6001 9.00309C12.6001 8.87856 12.5507 8.75912 12.4628 8.67101L9.33196 5.53814C9.28835 5.49447 9.23657 5.45983 9.17957 5.43619C9.12257 5.41256 9.06148 5.40039 8.99978 5.40039C8.93809 5.40039 8.877 5.41256 8.82 5.43619C8.763 5.45983 8.71122 5.49447 8.66761 5.53814H8.66823Z"
                    fill="#143584" />
                <rect x="-0.5" y="0.5" width="17" height="17" transform="matrix(-1 0 0 1 17 0)" stroke="#143584" />
            </svg>
        </div>
    </section>
</template>
<style scoped>
.blog {
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

.blog .image-holder {
    position: relative;
    display: flex;
}

.blog .label {
    position: absolute;
    bottom: 0;
    left: 0;
    background-color: var(--color-primary);
    color: white;
    padding: 0.5em 1em;
    font-size: var(--small-font);
    border-radius: 12px 12px 0 0;
}

.blog .health {
    width: 50px;
    height: auto;
    position: absolute;
    right: 0.4rem;
    bottom: 0.5rem;
}




/* ----------------- icon -button ------------- */


.blog .icons-button {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 0.6rem;
    display: none;
}

.blog .icons-button svg {
    width: 24px;
    height: 24px;
}



@media only screen and (max-width: 800px) {
    .blog .page {
        display: grid;
        gap: 2rem;
        grid-template-columns: 100%;
    }

    .blog .icons-button {
        display: flex;
    }
}

@media only screen and (max-width: 600px) {
    .blog .card {
        min-width: 100%;
        width: 100%;
    }

    .icons-button {
        display: block;
    }
}
</style>