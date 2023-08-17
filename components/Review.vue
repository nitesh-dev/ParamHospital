
<script setup lang='ts'>

import review1 from '~/public/images/review/review1.jpg'
import review2 from '~/public/images/review/review2.jpg'
import review3 from '~/public/images/review/review3.jpg'
import review4 from '~/public/images/review/review4.jpg'
import review5 from '~/public/images/review/review5.jpg'

const slideContent = Array<{
    image: string,
    name: string,
    rating: number,
    text: string
}>()



slideContent.push({
    image: review1,
    name: 'James',
    rating: 5,
    text: ''
})

slideContent.push({
    image: review2,
    name: 'Oliver',
    rating: 5,
    text: ''
})

slideContent.push({
    image: review3,
    name: 'Harshad Mavani',
    rating: 5,
    text: ''
})

slideContent.push({
    image: review4,
    name: 'Noah',
    rating: 5,
    text: ''
})

slideContent.push({
    image: review5,
    name: 'Emma',
    rating: 5,
    text: ''
})


const autoPlay = {
    delay: 3000,
    disableOnInteraction: true,
}


const navigation = {
    nextEl: '.swiper-button-next',
    prevEl: '.swiper-button-prev',
}


const effect = {
    prev: {
        shadow: false,
        translate: ['-100%', 0, -1],
    },
    next: {
        translate: ['100%', 0, 0],
    },
}

</script>
<template>
    <section class="review">
        <div class="page">
            <h5>Review</h5>
            <h2>Word From Our Customers</h2>
            <div class="container">
                <Swiper :modules="[SwiperAutoplay, SwiperEffectCreative, SwiperNavigation]" :slides-per-view="1"
                    :loop="true" :effect="'creative'" :autoplay="autoPlay" :navigation="navigation" :creative-effect="effect">
                    <SwiperSlide v-for="slide, index in slideContent" :key="index">

                        <div class="profile">
                            <img :src="slide.image" :alt="slide.name">
                            <h4>{{ slide.name }}</h4>
                            <div class="rating">
                                <svg v-for="item in 5" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 14 13" fill="none">
                                    <g clip-path="url(#clip0_145_1355)">
                                        <path
                                            d="M13.155 4.64941L9.15855 4.03895L7.36726 0.223453C7.23347 -0.0614635 6.76601 -0.0614635 6.63222 0.223453L4.84147 4.03895L0.845052 4.64941C0.771265 4.66075 0.702028 4.69219 0.644943 4.7403C0.587858 4.78841 0.545132 4.85132 0.521458 4.92212C0.497783 4.99292 0.494075 5.06887 0.51074 5.14164C0.527406 5.21441 0.5638 5.28118 0.615927 5.33462L3.51926 8.31054L2.83297 12.5177C2.82072 12.5929 2.82988 12.6701 2.85941 12.7404C2.88894 12.8106 2.93766 12.8712 2.99998 12.9151C3.0623 12.959 3.13572 12.9845 3.21184 12.9886C3.28796 12.9928 3.36371 12.9754 3.43043 12.9385L7.00001 10.9658L10.5696 12.9391C10.6363 12.976 10.7121 12.9933 10.7882 12.9892C10.8643 12.985 10.9377 12.9595 11 12.9156C11.0624 12.8717 11.1111 12.8112 11.1406 12.7409C11.1701 12.6706 11.1793 12.5934 11.1671 12.5182L10.4808 8.31108L13.3841 5.33516C13.4364 5.28174 13.4729 5.21493 13.4897 5.14208C13.5064 5.06923 13.5027 4.99318 13.4791 4.92228C13.4554 4.85138 13.4126 4.7884 13.3554 4.74025C13.2982 4.69211 13.2289 4.66068 13.155 4.64941Z"
                                            fill="#F0B200" />
                                    </g>
                                    <defs>
                                        <clipPath id="clip0_145_1355">
                                            <rect width="13" height="13" fill="white" transform="translate(0.5)" />
                                        </clipPath>
                                    </defs>
                                </svg>
                            </div>
                            <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has
                                been the industry's standard dummy text ever since the 1500s, when an unknown printer took a
                                galley of type and scrambled it to make a type specimen book. </p>

                        </div>

                    </SwiperSlide>
                </Swiper>

                <div class="button swiper-button-prev">
                    <svg xmlns="http://www.w3.org/2000/svg" width="17" height="17" viewBox="0 0 17 17" fill="none">
                        <path
                            d="M10.2962 10.6806C10.421 10.8054 10.4912 10.9747 10.4912 11.1512C10.4912 11.3278 10.421 11.4971 10.2962 11.6219C10.1714 11.7467 10.0021 11.8168 9.82556 11.8168C9.64904 11.8168 9.47974 11.7467 9.35492 11.6219L6.7034 8.97037C6.64127 8.90874 6.59196 8.83543 6.5583 8.75465C6.52465 8.67387 6.50732 8.58723 6.50732 8.49972C6.50732 8.41222 6.52465 8.32557 6.5583 8.2448C6.59196 8.16402 6.64127 8.0907 6.7034 8.02908L9.35492 5.37756C9.41672 5.31576 9.4901 5.26673 9.57085 5.23328C9.6516 5.19983 9.73815 5.18262 9.82556 5.18262C9.91297 5.18262 9.99952 5.19983 10.0803 5.23328C10.161 5.26673 10.2344 5.31576 10.2962 5.37756C10.358 5.43937 10.407 5.51274 10.4405 5.5935C10.4739 5.67425 10.4912 5.7608 10.4912 5.84821C10.4912 5.93561 10.4739 6.02217 10.4405 6.10292C10.407 6.18367 10.358 6.25705 10.2962 6.31885L8.10871 8.49972L10.2962 10.6806Z" />
                    </svg>
                </div>
                <div class="button swiper-button-next">
                    <svg xmlns="http://www.w3.org/2000/svg" width="17" height="17" viewBox="0 0 17 17" fill="none">
                        <path
                            d="M6.70379 10.6806C6.57897 10.8054 6.50885 10.9747 6.50885 11.1512C6.50885 11.3278 6.57897 11.4971 6.70379 11.6219C6.82862 11.7467 6.99791 11.8168 7.17444 11.8168C7.35096 11.8168 7.52026 11.7467 7.64508 11.6219L10.2966 8.97037C10.3587 8.90874 10.408 8.83543 10.4417 8.75465C10.4753 8.67387 10.4927 8.58723 10.4927 8.49972C10.4927 8.41222 10.4753 8.32557 10.4417 8.2448C10.408 8.16402 10.3587 8.0907 10.2966 8.02908L7.64508 5.37756C7.58328 5.31576 7.5099 5.26673 7.42915 5.23328C7.3484 5.19983 7.26185 5.18262 7.17444 5.18262C7.08703 5.18262 7.00048 5.19983 6.91973 5.23328C6.83897 5.26673 6.7656 5.31576 6.70379 5.37756C6.64199 5.43937 6.59296 5.51274 6.55951 5.5935C6.52606 5.67425 6.50885 5.7608 6.50885 5.84821C6.50885 5.93561 6.52606 6.02217 6.55951 6.10292C6.59296 6.18367 6.64199 6.25705 6.70379 6.31885L8.89129 8.49972L6.70379 10.6806Z" />
                    </svg>
                </div>
            </div>

        </div>
        <div class="background"></div>
        <img class="left" src="../public/images/outlines/heart.png">
        <img class="right" src="../public/images/outlines/heart.png">

        <!-- profile icons -->
        <img class="mini top-left" src="../public/images/review/review2.jpg">
        <img class="mini top-right" src="../public/images/review/review5.jpg">
        <img class="mini bottom-left" src="../public/images/review/review1.jpg">
        <img class="mini bottom-right" src="../public/images/review/review4.jpg">

    </section>
</template>
<style scoped>
.review {
    margin: 3rem 0;
    position: relative;
    margin-top: 3rem !important;
}

.review .page {
    padding-top: 1rem;
    padding-bottom: 3rem;
}

.review .container {
    position: relative;
}


.review h5 {
    text-align: center;
    color: var(--color-primary);
    margin-bottom: 0.5em;
}

.review h2 {
    text-align: center;
    margin-top: 0;
    margin-bottom: 2em;
}

.review .background {
    background-color: #EDF5FF;
    position: absolute;
    z-index: -4;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
}

.review .page {
    min-height: 400px;
}

.review>.left,
.review>.right {
    position: absolute;
    height: 100%;
    opacity: 0.15;
    top: 0;
}

.review>.left {
    left: 0;
    transform: rotateY(180deg);
}

.review>.right {
    right: 0;
}



/* --------------------------- mini icons ---------------- */

.review .mini {
    width: 40px;
    height: 40px;
    border-radius: 50%;
    position: absolute;
    z-index: -1;
}

.review .top-left {
    left: 20%;
    top: 110px;
}

.review .top-right {
    right: 20%;
    top: 70px;
}

.review .bottom-left {
    left: 10%;
    bottom: 40px;
}


.review .bottom-right {
    right: 5%;
    bottom: 70px;
}






/* -------------------------- profile ------------------ */

.review .profile img {
    width: 80px;
    height: 80px;
    border-radius: 50%;
    object-fit: cover;
    display: block;
    margin: auto;
}

.review .profile h4 {
    text-align: center;
    margin: 0.8em 0;
    color: black;
}

.review .profile p {
    text-align: center;
    width: 100%;
    max-width: 800px;
    margin: auto;
    margin-top: 1.5rem;
}

.review .rating {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 0.4rem;
}

.review .rating svg {
    width: 24px;
}



.review .swiper-button-prev::after,
.review .swiper-button-next::after {
    content: '';
}

.review .container .button {
    position: absolute;
    width: 50px;
    height: 50px;
    background-color: #d8e1ecc2;
    border-radius: 50%;
    fill: var(--color-on-surface-dark);
}

.review .container .button svg {
    fill: inherit;
    width: 32px;
}

.review .swiper-button-prev {
    left: 0;
    top: 50%;
    transform: translateY(-50%);
}

.review .swiper-button-next {
    right: 0;
    top: 50%;
    transform: translateY(-50%);
}






@media only screen and (max-width: 700px) {
    .review .mini {
        width: 28px;
        height: 28px;
        border-radius: 50%;
        position: absolute;
        z-index: -1;
    }

    .review .top-left {
        left: 20%;
        top: 110px;
    }

    .review .top-right {
        right: 20%;
        top: 150px;
    }

    .review .bottom-left {
        left: 10%;
        bottom: 140px;
    }


    .review .bottom-right {
        right: 5%;
        bottom: 150px;
    }
}
</style>