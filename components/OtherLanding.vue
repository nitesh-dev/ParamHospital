<script setup lang='ts'>
defineProps<{
    name: string
}>()
</script>
<template>
    <section class="landing">
        <div class="page">
            <h1>{{ name }}</h1>

            <div class="image-holder">
                <img src="../public/images/outlines/circles.png">
                <img src="../public/images/doctor.png">
            </div>
        </div>
        <div class="background"></div>
        <div class="circle"></div>
    </section>
</template>
<style scoped>
.landing {
    position: relative;
}

.landing h1 {
    font-size: calc(var(--big-font) - 4px);
}

.landing .background{
    position: absolute;
    z-index: -4;
    background-color: var(--color-surface-variant);
    height: 100%;
    width: 100%;
    left: 0;
    top: 0;
}

.landing .circle{
    position: absolute;
    z-index: -3;
    background-color: #5472b910;
    height: 250px;
    width: 250px;
    left: -60px;
    top: -60px;
    border-radius: 50%;
}

.landing .page {
    height: 200px;
    display: flex;
    align-items: center;
    position: relative;
}


.landing .image-holder{
    position: absolute;
    top: 0;
    right: 0;
    height: 100%;
    aspect-ratio: 1/1;
}


.landing .image-holder img:first-child{
    height: 100%;
    position: absolute;
    right: 0;
    top: 0;
}

.landing .image-holder img:last-child{
    height: 100%;
    position: absolute;
    right: 50%;
    top: 0;
    transform: translateX(50%);

}
</style>