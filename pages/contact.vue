<script setup lang='ts'>

</script>
<template>
    <Head>
        <Title>Contact Us</Title>
    </Head>
    <Header url="contact"></Header>
    <OtherLanding name="Contact"></OtherLanding>
    <div class="map">
        <Contact></Contact>
        <img src="../public/images/map.png" alt="map">
    </div>
    <br>
    <Footer></Footer>
</template>
<style scoped>

.map{
    position: relative;
    padding-bottom: 200px;
}

.map img{
    position: absolute;
    width: 100%;
    bottom: 0;
    z-index: -10;
    height: 510px;
    object-fit: cover;
}


</style>