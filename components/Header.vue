<script setup lang='ts'>
defineProps<{
    url: String
}>()


const navContainer = ref<HTMLDivElement>()

function toggleNav() {
    navContainer.value!!.classList.toggle('show')
}


</script>
<template>
    <header class="desktop">
        <div class="page">
            <div class="image-holder">
                <img src="../public/images/logo.png" alt="icon">
            </div>
            <div class="center">
                <div :class="{ 'active': url == '/' }">
                    <NuxtLink to="/">Home</NuxtLink>
                    <span></span>
                </div>
                <div :class="{ 'active': url == 'about' }">
                    <NuxtLink to="/about">About</NuxtLink>
                    <span></span>
                </div>

                <div :class="{ 'active': url == 'services' }">
                    <NuxtLink to="/services">Services</NuxtLink>
                    <span></span>
                </div>

                <div :class="{ 'active': url == 'facilities' }">
                    <NuxtLink to="/facilities">Facilities</NuxtLink>
                    <span></span>
                </div>

                <div :class="{ 'active': url == 'review' }">
                    <NuxtLink to="/review">Review</NuxtLink>
                    <span></span>
                </div>

                <div :class="{ 'active': url == 'team' }">
                    <NuxtLink to="/team">Team</NuxtLink>
                    <span></span>
                </div>

                <div :class="{ 'active': url == 'blog' }">
                    <NuxtLink to="/blog">Blog</NuxtLink>
                    <span></span>
                </div>

                <div :class="{ 'active': url == 'contact' }">
                    <NuxtLink to="/contact">Contact Us</NuxtLink>
                    <span></span>
                </div>
            </div>

            <NuxtLink to="/appointment"><ArrowButton text="Get Appointment" /></NuxtLink>
        </div>
    </header>

    <header class="phone">
        <div class="page">
            <div class="image-holder">
                <img src="../public/images/logo.png" alt="icon">
            </div>
            <button class="icon-button" @click="toggleNav()">
                <svg width="24" height="24" fill="none" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                    <path
                        d="M3 17h18a1 1 0 0 1 .117 1.993L21 19H3a1 1 0 0 1-.117-1.993L3 17h18H3Zm0-6 18-.002a1 1 0 0 1 .117 1.993l-.117.007L3 13a1 1 0 0 1-.117-1.993L3 11l18-.002L3 11Zm0-6h18a1 1 0 0 1 .117 1.993L21 7H3a1 1 0 0 1-.117-1.993L3 5h18H3Z" />
                </svg>
            </button>
        </div>
        <div ref="navContainer" class="nav-container">
            <div class="nav-background" @click="toggleNav()"></div>
            <div class="nav">
                <NuxtLink to="/">Home</NuxtLink>
                <NuxtLink to="/about">About Us</NuxtLink>
                <NuxtLink to="/services">Services</NuxtLink>
                <NuxtLink to="/facilities">Facilities</NuxtLink>
                <NuxtLink to="/review">Review</NuxtLink>
                <NuxtLink to="/team">Team</NuxtLink>
                <NuxtLink to="/blog">Blog</NuxtLink>
                <NuxtLink to="/contact">Contact Us</NuxtLink>

            </div>
        </div>
    </header>
</template>
<style scoped>
header {
    background-color: var(--color-surface);
    width: 100%;
    position: sticky;
    z-index: 100;
}

header .page {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 80px;
}


header .image-holder {
    position: relative;
    width: 110px;
    height: 60px;
}

header img {
    height: 50px;
    width: auto;
    position: absolute;
    top: 6px;
}




header .center {
    display: flex;
    gap: 1em;
}

header .center div {
    position: relative;
}

header .center span {
    position: absolute;
    width: 20px;
    height: 2px;
    background-color: transparent;
    bottom: -2px;
    left: 0;
}

header .center .active a {
    color: var(--color-primary);
    font-weight: bold;
}

header .center .active span {
    background-color: var(--color-primary);
}





/* --------------------------- phone -------------- */
.phone {
    display: none;
}


header.phone button{
    border: none;
    background-color: transparent;
}
header.phone .page {
    height: 60px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

header.phone .icon-button svg{
    fill: var(--color-primary);
}





/*  ------------------ nav -------------- */

header .nav-background {
    width: 100%;
    height: 100vh;
    position: fixed;
    z-index: 199;
    top: 0;
    right: 0;
    display: none;
    background-color: transparent;
}

header .nav {
    width: 250px;
    height: 100vh;
    position: fixed;
    z-index: 200;
    top: 0;
    right: 0;
    background-color: black;
    transform: translateX(100%);
    transition: all 200ms;
}

header .nav-container.show .nav {
    transform: translateX(0);
}

header .nav-container.show .nav-background {
    display: block;
    background-color: rgba(0, 0, 0, 0.35);
}

header .nav {
    padding: 2rem 1.5rem;
}

header .nav a {
    color: white;
    display: block;
    padding: 0.4em 0;
}





@media only screen and (max-width: 950px) {
    .desktop {
        display: none !important;
    }

    .phone {
        display: block;
    }
}
</style>