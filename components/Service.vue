<script setup lang='ts'>


const content = Array<{
    title: string,
    content: string
}>()

content.push({
    title: 'Joint Arthroscopy',
    content: 'a thin telescope with a light (arthroscope) is inserted into joints via a small incision to investigate joint problems. This is most commonly in the knee but other joints can also be investigated in this way. The arthroscope can be used to look for signs of arthritis and show possible damage to cartilage or ligaments. Minimally invasive surgery can be performed to repair damaged tissue by removing floating cartilage, torn ligaments or tissue around the joint that has become inflammed.'
})


content.push({
    title: 'Bone Fracture Fixation',
    content: 'surgery to stabilize broken bone using metal screws, pins, rods or plates to hold the bone in place. Many different techniques are used depending on the location, severity and type of fracture to ensure that the bones are stable, heal correctly and maintain function. A bone graft may be used where the bone has been shattered.'
})
content.push({
    title: 'Arthroplasty',
    content: 'the replacement of whole joints following damage due to osteoarthritis or rheumatoid arthritis. Knee and hip replacements are the most common operations. Newer techniques such as partial knee resurfacing are being used for patients in the early stages of osteoarthritis.'
})

content.push({
    title: 'Muscle or Tendon Repairs',
    content: 'Any soft tissue injuries following trauma, industrial injuries or chronic degenerative injuries can be repaired or removed depending on its severity & function.'
})

content.push({
    title: 'Corrective Surgery',
    content: 'These procedures correct problems of anatomical alignment which limit function and could cause long-term problems if left untreated. This surgery is often carried out on babies and children for congenital deformities.'
})

</script>
<template>
    <section class="service">
        <div class="page">
            <h5>Service</h5>
            <h2>Orthopedics & Trauma</h2>
            <p class="middle">Trauma and orthopaedic surgeons diagnose and treat a wide range of conditions of the
                musculoskeletal system. This includes bones and joints and their associated structures that enable movement
                - ligaments, tendons, muscles and nerves. Trauma and orthopaedic surgery is often abbreviated to T&O
                surgery.</p>
        </div>
        <div class="swiper">
            <h2>Swiper left</h2>
        </div>

        <div class="page">
            <h5>Our Departments</h5>
            <h2>Orthopedics & Trauma Surgery.</h2>
            <p class="middle">Trauma and orthopaedic surgeons diagnose and treat a wide range of conditions of the
                musculoskeletal system. This includes bones and joints and their associated structures that enable movement
                - ligaments, tendons, muscles and nerves. Trauma and orthopaedic surgery is often abbreviated to T&O
                surgery.
            </p>

            <br>
            <h3>Common procedures/intervention</h3>

            <div class="procedures">
                <div class="item" v-for="item in content">
                    <svg xmlns="http://www.w3.org/2000/svg" width="26" height="26" viewBox="0 0 26 26" fill="none">
                        <path
                            d="M25.7773 12.4227L17.9777 3.75647C17.8113 3.57274 17.5791 3.46875 17.3329 3.46875H12.1332C11.9658 3.46893 11.802 3.51744 11.6615 3.60845C11.521 3.69945 11.4098 3.82909 11.3411 3.98179C11.2025 4.29551 11.2597 4.66122 11.4885 4.91427L18.7663 13.0016L11.4885 21.0871C11.2597 21.3419 11.2007 21.7076 11.3411 22.0196C11.4815 22.3333 11.7918 22.5344 12.1332 22.5344H17.3329C17.5791 22.5344 17.8113 22.4287 17.9777 22.2484L25.7773 13.5822C26.0737 13.2529 26.0737 12.7502 25.7773 12.4227Z"
                            fill="#143584" />
                        <path
                            d="M14.5117 12.4227L6.71208 3.75647C6.54569 3.57274 6.31343 3.46875 6.06731 3.46875H0.867594C0.700187 3.46893 0.536392 3.51744 0.395883 3.60845C0.255374 3.69945 0.144127 3.82909 0.0755039 3.98179C-0.0631553 4.29551 -0.00595841 4.66122 0.222829 4.91427L7.5007 13.0016L0.222829 21.0871C-0.00595841 21.3419 -0.0648886 21.7076 0.0755039 22.0196C0.215896 22.3333 0.526146 22.5344 0.867594 22.5344H6.06731C6.31343 22.5344 6.54569 22.4287 6.71208 22.2484L14.5117 13.5822C14.808 13.2529 14.808 12.7502 14.5117 12.4227Z"
                            fill="#143584" />
                    </svg>
                    <div>
                        <h4>{{ item.title }}</h4>
                        <p>{{ item.content }}</p>
                    </div>
                </div>
            </div>

            <p class="middle">T&O surgeons have the opportunity to use the latest surgical technologies including minimally
                invasive techniques. Another new development is computer aided navigation during surgery which enables 3D
                mapping of a joint. This gives the surgeon a greater degree of accuracy when making incisions.
            </p>
        </div>
    </section>
</template>
<style scoped>
.service {
    margin: 4rem 0;
}

.service h5 {
    text-align: center;
    color: var(--color-primary);
    margin-bottom: 0.5rem;
}

.service h2 {
    text-align: center;
    margin-top: 0;
}

.service p.middle {
    text-align: center;
    max-width: 800px;
    margin: auto;
}


/* ------------------ swiper ------------- */
.service .swiper {
    min-height: 250px;
    background-color: rgb(238, 238, 238);
}





/* ------------- bottom ------- */

.service .procedures .item {
    display: grid;
    grid-template-columns: max-content 1fr;
    align-items: flex-start;
    gap: 1rem;
    margin-bottom: 1rem;
}


.service h3 {
    border-bottom: 1px solid rgb(224, 224, 224);
    width: max-content;
    padding-bottom: 0.6rem;
}

.service .item h4 {
    margin-top: 4px;
    margin-bottom: 0;
    color: var(--color-primary);
}

.service .item p {
    margin-top: 0.5em;
}

.service svg {
    width: 18px;
}
</style>