<script setup lang='ts'>

import opd1 from '~/public/images/facility/opd1.jpg'
import opd2 from '~/public/images/facility/opd2.jpg'
import opd3 from '~/public/images/facility/opd3.jpg'
import opd4 from '~/public/images/facility/opd4.jpg'
import opd5 from '~/public/images/facility/opd5.jpg'
import opd6 from '~/public/images/facility/opd6.jpg'
import opd7 from '~/public/images/facility/opd7.jpg'

const data = Array<{
    title: string,
    text: string,
    url: string,
    image: string
}>()

data.push({
    title: 'Hospital Reception',
    text: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry\'s. ',
    url: '#',
    image: opd1
})

data.push({
    title: 'Waiting Area',
    text: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry\'s. ',
    url: '#',
    image: opd2
})

data.push({
    title: 'Waiting Area',
    text: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry\'s. ',
    url: '#',
    image: opd3
})

data.push({
    title: 'Patient Check Up',
    text: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry\'s. ',
    url: '#',
    image: opd4
})

data.push({
    title: 'Patient Check Up',
    text: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry\'s. ',
    url: '#',
    image: opd5
})

data.push({
    title: 'Patient Check Up',
    text: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry\'s. ',
    url: '#',
    image: opd6
})

data.push({
    title: 'Patient Check Up',
    text: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry\'s. ',
    url: '#',
    image: opd7
})

const scrollContainer = ref<HTMLDivElement>()

function scrollLeft() {
    if (scrollContainer.value == undefined) return
    scrollContainer.value.scrollLeft = 0
}

function scrollRight() {
    if (scrollContainer.value == undefined) return
    scrollContainer.value.scrollLeft = scrollContainer.value.scrollWidth
}






</script>
<template>
    <section class="opd">
        <div class="page">
            <h5>Param Hospital</h5>
            <h2>OPD</h2>
            <p class="middle">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has
                been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type
                and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap
                into electronic typesetting, remaining essentially unchanged
            </p>

            <div class="phone">
                <h5>Param Hospital</h5>
                <h2>Our Facilities</h2>
            </div>
            <div class="container hide-scroll" ref="scrollContainer">
                <div v-for="item, index in data" class="card">
                    <div>
                        <img :src="item.image">
                        <div class="content">
                            <h4>{{ item.title }}</h4>
                            <p>{{ item.text }}</p>
                            <span class="label">0{{ index + 1 }}</span>
                        </div>
                    </div>
                </div>
            </div>
            <div class="button-holder">
                <button class="primary primary-outline icon left" @click="scrollLeft()">
                    <svg width="16" height="16" viewBox="0 0 18 18" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path fill-rule="evenodd" clip-rule="evenodd"
                            d="M3.34102 2.77857C3.18301 2.93677 3.09426 3.15123 3.09426 3.37482C3.09426 3.59841 3.18301 3.81287 3.34102 3.97107L8.36864 8.99982L3.33989 14.0286C3.18627 14.1878 3.10132 14.4009 3.10335 14.6222C3.10537 14.8434 3.19421 15.055 3.35072 15.2114C3.50724 15.3677 3.7189 15.4564 3.94013 15.4582C4.16136 15.46 4.37446 15.3748 4.53352 15.2211L10.1585 9.59607C10.3165 9.43787 10.4053 9.22341 10.4053 8.99982C10.4053 8.77623 10.3165 8.56177 10.1585 8.40357L4.53352 2.77857C4.45516 2.70016 4.36212 2.63796 4.25972 2.59553C4.15731 2.55309 4.04755 2.53125 3.9367 2.53125C3.82586 2.53125 3.71609 2.55309 3.61369 2.59553C3.51129 2.63796 3.41825 2.70016 3.33989 2.77857H3.34102Z" />
                        <path fill-rule="evenodd" clip-rule="evenodd"
                            d="M8.96602 2.77857C8.80801 2.93677 8.71926 3.15123 8.71926 3.37482C8.71926 3.59841 8.80801 3.81287 8.96602 3.97107L13.9936 8.99982L8.96489 14.0286C8.81127 14.1878 8.72632 14.4009 8.72835 14.6222C8.73037 14.8434 8.81921 15.055 8.97572 15.2114C9.13224 15.3677 9.3439 15.4564 9.56513 15.4582C9.78636 15.46 9.99946 15.3748 10.1585 15.2211L15.7835 9.59607C15.9415 9.43787 16.0303 9.22341 16.0303 8.99982C16.0303 8.77623 15.9415 8.56177 15.7835 8.40357L10.1585 2.77857C10.0802 2.70016 9.98712 2.63796 9.88472 2.59553C9.78231 2.55309 9.67255 2.53125 9.5617 2.53125C9.45085 2.53125 9.34109 2.55309 9.23869 2.59553C9.13629 2.63796 9.04325 2.70016 8.96489 2.77857H8.96602Z" />
                    </svg>
                </button>
                <button class="primary primary-outline icon" @click="scrollRight()">
                    <svg width="16" height="16" viewBox="0 0 18 18" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path fill-rule="evenodd" clip-rule="evenodd"
                            d="M3.34102 2.77857C3.18301 2.93677 3.09426 3.15123 3.09426 3.37482C3.09426 3.59841 3.18301 3.81287 3.34102 3.97107L8.36864 8.99982L3.33989 14.0286C3.18627 14.1878 3.10132 14.4009 3.10335 14.6222C3.10537 14.8434 3.19421 15.055 3.35072 15.2114C3.50724 15.3677 3.7189 15.4564 3.94013 15.4582C4.16136 15.46 4.37446 15.3748 4.53352 15.2211L10.1585 9.59607C10.3165 9.43787 10.4053 9.22341 10.4053 8.99982C10.4053 8.77623 10.3165 8.56177 10.1585 8.40357L4.53352 2.77857C4.45516 2.70016 4.36212 2.63796 4.25972 2.59553C4.15731 2.55309 4.04755 2.53125 3.9367 2.53125C3.82586 2.53125 3.71609 2.55309 3.61369 2.59553C3.51129 2.63796 3.41825 2.70016 3.33989 2.77857H3.34102Z" />
                        <path fill-rule="evenodd" clip-rule="evenodd"
                            d="M8.96602 2.77857C8.80801 2.93677 8.71926 3.15123 8.71926 3.37482C8.71926 3.59841 8.80801 3.81287 8.96602 3.97107L13.9936 8.99982L8.96489 14.0286C8.81127 14.1878 8.72632 14.4009 8.72835 14.6222C8.73037 14.8434 8.81921 15.055 8.97572 15.2114C9.13224 15.3677 9.3439 15.4564 9.56513 15.4582C9.78636 15.46 9.99946 15.3748 10.1585 15.2211L15.7835 9.59607C15.9415 9.43787 16.0303 9.22341 16.0303 8.99982C16.0303 8.77623 15.9415 8.56177 15.7835 8.40357L10.1585 2.77857C10.0802 2.70016 9.98712 2.63796 9.88472 2.59553C9.78231 2.55309 9.67255 2.53125 9.5617 2.53125C9.45085 2.53125 9.34109 2.55309 9.23869 2.59553C9.13629 2.63796 9.04325 2.70016 8.96489 2.77857H8.96602Z" />
                    </svg>
                </button>
            </div>
        </div>
    </section>
</template>
<style scoped>
.opd p.middle {
    text-align: center;
    max-width: 1000px;
    margin: auto;
    margin-bottom: 2rem;
}

.opd {
    margin: 4rem 0;
}

.opd .phone {
    display: none;
}

.opd h5 {
    text-align: center;
    color: var(--color-primary);
    margin-bottom: 0.5rem;
}

.opd h2 {
    text-align: center;
    margin-top: 0;
}


.opd .container {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 8px;
    /* overflow: auto; */
}

.opd .card>div {
    border-radius: 8px;
    margin: 0.5rem;
    box-shadow: 0px 0px 40px 0px rgba(0, 0, 0, 0.1);
    position: relative;
}

.opd .card img {
    border-radius: 8px 8px 0 0;
    width: 100%;
    height: 290px;
    object-fit: cover;

}

.opd .content {
    padding: 34px;
    padding-bottom: 2rem;
}

.opd .content h4 {
    margin: 0;
    color: var(--color-primary);
}

.opd .content a {
    color: var(--color-primary);
}

.opd .content .label {
    font-size: var(--big-font);
    font-weight: bold;
    position: absolute;
    right: 1rem;
    bottom: 0.2rem;
    color: rgba(0, 0, 0, 0.1);
}

.opd .button-holder {
    display: flex;
    gap: 1rem;
    justify-content: center;
    display: none;
}

.opd .button-holder button {
    padding: 0.5rem;
    border-radius: 0;
}

.opd button.left svg {
    rotate: 180deg;
}


@media only screen and (max-width: 1000px) {
    .opd .container {
        grid-template-columns: 1fr 1fr;
    }
}



@media only screen and (max-width: 700px) {
    .opd .container {
        display: flex;
        overflow: auto;
        flex-wrap: nowrap;
        justify-content: unset;

    }

    .opd .card {
        min-width: 400px;
    }


    .opd .card>div {
        border-radius: 8px;
        margin: 1rem 0.5rem;
        box-shadow: 0px 0px 40px 0px rgba(0, 0, 0, 0.1);
        position: relative;
    }

    .opd .button-holder {
        display: flex;
    }

    .opd .phone {
        display: block;
    }
}
</style>