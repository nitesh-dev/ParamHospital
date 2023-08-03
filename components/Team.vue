<script setup lang='ts'>
</script>
<template>
    <section class="team">
        <div class="page">
            <h5>Our Team</h5>
            <h2>Meet with our best experts</h2>
            <div class="card-container">
                <div class="card" :class="{'active': index == 0}" v-for="item, index in 3">
                    <div>
                        <img src="../public/images/members/member1.png" alt="member">
                        <div class="detail">
                            <p>Dr. Bharat Sutariya</p>
                            <hr>
                            <div class="social">
                                <!-- facebook -->
                                <a href="#">
                                    <svg xmlns="http://www.w3.org/2000/svg" width="21" height="20" viewBox="0 0 21 20"
                                        fill="none">
                                        <path
                                            d="M8.58018 11.0395H6.60018C6.28018 11.0395 6.18018 10.9195 6.18018 10.6195V8.19953C6.18018 7.87953 6.30018 7.77953 6.60018 7.77953H8.58018V6.01953C8.58018 5.21953 8.72018 4.45953 9.12018 3.75953C9.54018 3.03953 10.1402 2.55953 10.9002 2.27953C11.4002 2.09953 11.9002 2.01953 12.4402 2.01953H14.4002C14.6802 2.01953 14.8002 2.13953 14.8002 2.41953V4.69953C14.8002 4.97953 14.6802 5.09953 14.4002 5.09953C13.8602 5.09953 13.3202 5.09953 12.7802 5.11953C12.2402 5.11953 11.9602 5.37953 11.9602 5.93953C11.9402 6.53953 11.9602 7.11953 11.9602 7.73953H14.2802C14.6002 7.73953 14.7202 7.85953 14.7202 8.17953V10.5995C14.7202 10.9195 14.6202 11.0195 14.2802 11.0195H11.9602V17.5395C11.9602 17.8795 11.8602 17.9995 11.5002 17.9995H9.00018C8.70018 17.9995 8.58018 17.8795 8.58018 17.5795V11.0395Z" />
                                    </svg>
                                </a>

                                <!-- instagram -->
                                <a href="#"><svg xmlns="http://www.w3.org/2000/svg" width="19" height="18"
                                        viewBox="0 0 19 18" fill="none">
                                        <g clip-path="url(#clip0_145_2049)">
                                            <path
                                                d="M14.7324 3.33105C14.4915 3.33105 14.2954 3.52712 14.2954 3.76805C14.2954 4.00897 14.4915 4.20504 14.7324 4.20504C14.9734 4.20504 15.1694 4.00901 15.1694 3.76805C15.1694 3.52709 14.9734 3.33105 14.7324 3.33105ZM9.50005 5.12631C7.36389 5.12631 5.62598 6.86422 5.62598 9.00039C5.62598 11.1366 7.36389 12.8745 9.50005 12.8745C11.6363 12.8745 13.3742 11.1366 13.3742 9.00042C13.3742 6.86426 11.6363 5.12631 9.50005 5.12631Z" />
                                            <path
                                                d="M13.5656 0H5.43443C2.71358 0 0.5 2.21358 0.5 4.93446V13.0656C0.5 15.7865 2.71358 18 5.43443 18H13.5656C16.2865 18 18.5 15.7864 18.5 13.0656V4.93446C18.5 2.21358 16.2865 0 13.5656 0ZM9.5 13.9371C6.77768 13.9371 4.56297 11.7223 4.56297 9C4.56297 6.27768 6.77771 4.06301 9.5 4.06301C12.2223 4.06301 14.4371 6.27771 14.4371 9C14.4371 11.7223 12.2223 13.9371 9.5 13.9371ZM14.7323 5.26767C13.9053 5.26767 13.2324 4.59478 13.2324 3.7677C13.2324 2.94061 13.9053 2.26768 14.7323 2.26768C15.5594 2.26768 16.2323 2.94057 16.2323 3.76766C16.2323 4.59475 15.5594 5.26767 14.7323 5.26767Z" />
                                        </g>
                                        <defs>
                                            <clipPath id="clip0_145_2049">
                                                <rect width="18" height="18" transform="translate(0.5)" />
                                            </clipPath>
                                        </defs>
                                    </svg></a>

                                <!-- linkedin -->
                                <a href="#"><svg xmlns="http://www.w3.org/2000/svg" width="20" height="21"
                                        viewBox="0 0 20 21" fill="none">
                                        <path
                                            d="M18 18.5V12.64C18 9.76 17.38 7.56 14.02 7.56C12.4 7.56 11.32 8.44 10.88 9.28H10.84V7.82H7.66V18.5H10.98V13.2C10.98 11.8 11.24 10.46 12.96 10.46C14.66 10.46 14.68 12.04 14.68 13.28V18.48H18V18.5ZM2.26 7.82H5.58V18.5H2.26V7.82ZM3.92 2.5C2.86 2.5 2 3.36 2 4.42C2 5.48 2.86 6.36 3.92 6.36C4.98 6.36 5.84 5.48 5.84 4.42C5.84 3.36 4.98 2.5 3.92 2.5Z" />
                                    </svg></a>

                                <!-- twitter -->
                                <a href="#"><svg xmlns="http://www.w3.org/2000/svg" width="20" height="21"
                                        viewBox="0 0 20 21" fill="none">
                                        <path
                                            d="M17.98 5.54C17.38 5.8 16.76 5.98 16.1 6.06C16.78 5.66 17.3 5.02 17.54 4.24C16.9 4.62 16.2 4.88 15.46 5.04C14.86 4.4 14 4 13.06 4C11.24 4 9.77998 5.48 9.77998 7.28C9.77998 7.54 9.79998 7.78 9.85998 8.02C7.13998 7.9 4.73998 6.58 3.11998 4.6C1.95998 6.68 3.25998 8.4 4.11998 8.98C3.59998 8.98 3.07998 8.82 2.63998 8.58C2.63998 10.2 3.77998 11.54 5.25998 11.84C4.93998 11.94 4.21998 12 3.77998 11.9C4.19998 13.2 5.41998 14.16 6.83998 14.18C5.71998 15.06 4.07998 15.76 1.97998 15.54C3.43998 16.48 5.15998 17.02 7.01998 17.02C13.06 17.02 16.34 12.02 16.34 7.7C16.34 7.56 16.34 7.42 16.32 7.28C17 6.78 17.56 6.2 17.98 5.54Z" />
                                    </svg></a>
                            </div>

                            <svg class="arrow" xmlns="http://www.w3.org/2000/svg" width="22" height="22" viewBox="0 0 22 22"
                                fill="none">
                                <path
                                    d="M21 0H1.41421C0.523309 0 0.0771432 1.07714 0.707108 1.70711L20.2929 21.2929C20.9229 21.9229 22 21.4767 22 20.5858V1C22 0.447715 21.5523 0 21 0Z"
                                     />
                            </svg>
                        </div>
                    </div>

                </div>
            </div>
            <ArrowButton text="View All"></ArrowButton>
        </div>
    </section>
</template>
<style scoped>
.team h5 {
    color: var(--color-primary);
    text-align: center;
    margin-bottom: 0.5em;
}

.team button{
    margin: auto;
    margin-top: -1rem;
}

.team h2 {
    margin-top: 0;
    text-align: center;
}

.team .card-container {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 1rem;
    margin-top: 2rem;
}

.team .card img {
    width: 100%;
    aspect-ratio: 150/160;
    object-fit: cover;
}

.team .detail {
    background-color: white;
    width: 200px;
    padding: 0.5rem;
    margin: auto;
    transform: translateY(-50%);
    border-radius: 6px;
    position: relative;
    box-shadow: 0px 0px 40px 0px rgba(0, 0, 0, 0.08);
}

.team .detail p {
    text-align: center;
    color: var(--color-primary);
    font-weight: bold;
    margin-bottom: 0.5em;
}

.team .detail hr {
    border: none;
    border-bottom: 1px solid rgb(233, 233, 233);
    width: 80%;
}

.team .social {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 0.4rem;

}

.team .social a {
    width: 32px;
    height: 32px;
    display: flex;
    align-items: center;
    justify-content: center;
    fill: var(--color-primary);
    background-color: #e7eeffda;
    border-radius: 50%;
}

.team .arrow {
    position: absolute;
    top: 8px;
    right: 8px;
    width: 14px;
    fill: var(--color-primary);
}

.team .social svg {
    fill: inherit;
    width: 16px;
}



/* ---------------------active ---------------- */
.team .card.active .detail {
    background-color: var(--color-primary);
}

.team .card.active .detail p {
    color: white;
}

.team .card.active .detail hr {
    border: none;
    border-bottom: 1px solid rgba(233, 233, 233, 0.37);
    width: 80%;
}


.team .card.active .social a {
    fill: white;
    background-color: #ffffff31;
}

.team .card.active .arrow {
    fill: white;
}
</style>