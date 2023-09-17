<script setup lang='ts'>

import expert1 from '~/public/images/profiles/expert1.jpg'
import expert2 from '~/public/images/profiles/expert2.jpg'
import expert3 from '~/public/images/profiles/expert3.jpg'
import expert4 from '~/public/images/profiles/expert4.jpg'
import expert5 from '~/public/images/profiles/expert5.jpg'

const data = Array<{
    heading: string,
    name: string,
    images: Array<string>,
    info: Array<string>,
    bio: string

}>()


data.push({
    heading: 'Orthopaedic Surgeon',
    name: 'Dr. Bharat Sutariya',
    images: [expert1],
    info: [
        'MS (Ortho), FARS (Germany)',
        'Director & C.E.O',
        'M.B.B.S - B.J Medical Hospital',
        'M.S (Ortho) - V.S Medical College',
        'MBA in Hospital Management - Pune',
        'Fellowship - Arthroplasty (Germany & Canada), Arthroscopy (Taiwan & Germany)'
    ],
    bio: 'Dr. Bharat Sutariya, the Director of Param Hospital is practicing as orthopaedic surgeon, joint replacement surgeon and arthroscopist as well since more than 10 years. During this duration he has a rich experience and exposure of simple & comminuted fractures, primary & revision replacement surgeries and variety of sports related surgeries as an arthroscopist. He has a good skill and success ratio of more than 5,000 replacement surgeries and 5,000 arthroscopic ligament injuries, meniscal repairs, torn rotator cuff and labrum.'
})








data.push({
    heading: 'General & Laparoscopic Surgeon',
    name: 'Dr. Yagnesh Vaghani',
    images: [expert2],
    info: [
        'MS (General Surgery)',
        'FMAS, FIAGES, FICPS',
        'Consulting General & Laparoscopic Surgeon',
        'M.B.B.S - SMIMER College, Surat',
        'M.S (Surgery) - SMIMER College, Surat'
    ],
    bio: 'Having 8 years of experience in General Surgery & Laparoscopy. Treated various challenging cases of stomach & intestines with his unique decisive treatment abilities. A good surgical hand in procedures of GI Tract and anorectal conditions, kidney / bladder stones, tumours'
})


data.push({
    heading: 'Physiotherapist',
    name: 'Dr. Amit Butani',
    images: [expert3],
    info: [
        'B. Physio',
        'Chief Physiotherapist (Since Dec’ 2017)',
        'B.P.Th – St. Jhon’s College of Physiotherapy (Bangalore)',
        'Former Physiotherapist – Shiroya Orthopaedic Hospital & Trauma Centre (Jan’ 2010 to March’ 2013)',
        'Jivani Orthopaedic Hospital & Joint Replacement and Arthroscopy Centre (April’ 2013 to Nov’ 2017)'
    ],
    bio: 'With 10 years rich experience in physiotherapy, he has mastered skills to rehabilitate the patients of Post Traumatic Orthopaedic cases, Arthroplasty & Arthroscopy patients and Spine trauma patients. Besides the physiotherapy, he had also assisted various orthopaedic surgeries, joint replacement & arthroscopic procedure to enrich the clinical orientation of every possible joints & its structure. He had served as honorary Physiotherapist in IWAS world games 2009 Bangalore.'
})



data.push({
    heading: 'Administrator',
    name: 'Dr. Hitesh Jagda',
    images: [expert4],
    info: [
        'Qualifications'
    ],
    bio: 'Our administrator with experience of 25 years in medical field. Plays key role in hospital management and also serves as chief RMO with 16 years experience in solely orthopaedics.'
})



data.push({
    heading: 'Physician',
    name: 'Dr. Chandresh Vadadoriya',
    images: [expert5],
    info: [
        'MD (Medicine)',
        'Consulting Physician',
        'M.B.B.S – BJ Medical Hospital',
        'MD (Medicine) – BJ Medical Hospital',
        'Former Physician – Lokhat Hospital, Surat; Dev Children & Multi-speciality Hospital',
        'I.C.U registrar – Shrey Hospital; Shardaben municipal hospital, Ahmedabad'

    ],
    bio: 'A very dynamic & enthusiastic professional with rich knowledge & experience in various Heart Diseases, renal problems & endocrine conditions, epidemics, seasonal flues and fever varieties. Plays vital role in managing critical patients with his advanced clinical approaches. Specially interested in treating ICU patients with ventilators.'
})





</script>
<template>
    <Head>
        <Title>Team</Title>
    </Head>
    <Header url="team"></Header>
    <OtherLanding name="Team"></OtherLanding>
    <section class="team">
        <div class="page">
            <h5>Our Team</h5>
            <h2>Meet with our best experts</h2>
            <div class="card" v-for="item in data">
                <h4>{{ item.heading }}</h4>
                <div class="inner-card">
                    <div class="image-container">

                        <div class="image-holder">
                            <img :src="item.images[0]">
                            <div class="outline"></div>
                        </div>

                        <div class="button-holder">
                            <button class="primary primary-outline icon left">
                                <svg width="16" height="16" viewBox="0 0 18 18" fill="none"
                                    xmlns="http://www.w3.org/2000/svg">
                                    <path fill-rule="evenodd" clip-rule="evenodd"
                                        d="M3.34102 2.77857C3.18301 2.93677 3.09426 3.15123 3.09426 3.37482C3.09426 3.59841 3.18301 3.81287 3.34102 3.97107L8.36864 8.99982L3.33989 14.0286C3.18627 14.1878 3.10132 14.4009 3.10335 14.6222C3.10537 14.8434 3.19421 15.055 3.35072 15.2114C3.50724 15.3677 3.7189 15.4564 3.94013 15.4582C4.16136 15.46 4.37446 15.3748 4.53352 15.2211L10.1585 9.59607C10.3165 9.43787 10.4053 9.22341 10.4053 8.99982C10.4053 8.77623 10.3165 8.56177 10.1585 8.40357L4.53352 2.77857C4.45516 2.70016 4.36212 2.63796 4.25972 2.59553C4.15731 2.55309 4.04755 2.53125 3.9367 2.53125C3.82586 2.53125 3.71609 2.55309 3.61369 2.59553C3.51129 2.63796 3.41825 2.70016 3.33989 2.77857H3.34102Z" />
                                    <path fill-rule="evenodd" clip-rule="evenodd"
                                        d="M8.96602 2.77857C8.80801 2.93677 8.71926 3.15123 8.71926 3.37482C8.71926 3.59841 8.80801 3.81287 8.96602 3.97107L13.9936 8.99982L8.96489 14.0286C8.81127 14.1878 8.72632 14.4009 8.72835 14.6222C8.73037 14.8434 8.81921 15.055 8.97572 15.2114C9.13224 15.3677 9.3439 15.4564 9.56513 15.4582C9.78636 15.46 9.99946 15.3748 10.1585 15.2211L15.7835 9.59607C15.9415 9.43787 16.0303 9.22341 16.0303 8.99982C16.0303 8.77623 15.9415 8.56177 15.7835 8.40357L10.1585 2.77857C10.0802 2.70016 9.98712 2.63796 9.88472 2.59553C9.78231 2.55309 9.67255 2.53125 9.5617 2.53125C9.45085 2.53125 9.34109 2.55309 9.23869 2.59553C9.13629 2.63796 9.04325 2.70016 8.96489 2.77857H8.96602Z" />
                                </svg>
                            </button>
                            <button class="primary primary-outline icon">
                                <svg width="16" height="16" viewBox="0 0 18 18" fill="none"
                                    xmlns="http://www.w3.org/2000/svg">
                                    <path fill-rule="evenodd" clip-rule="evenodd"
                                        d="M3.34102 2.77857C3.18301 2.93677 3.09426 3.15123 3.09426 3.37482C3.09426 3.59841 3.18301 3.81287 3.34102 3.97107L8.36864 8.99982L3.33989 14.0286C3.18627 14.1878 3.10132 14.4009 3.10335 14.6222C3.10537 14.8434 3.19421 15.055 3.35072 15.2114C3.50724 15.3677 3.7189 15.4564 3.94013 15.4582C4.16136 15.46 4.37446 15.3748 4.53352 15.2211L10.1585 9.59607C10.3165 9.43787 10.4053 9.22341 10.4053 8.99982C10.4053 8.77623 10.3165 8.56177 10.1585 8.40357L4.53352 2.77857C4.45516 2.70016 4.36212 2.63796 4.25972 2.59553C4.15731 2.55309 4.04755 2.53125 3.9367 2.53125C3.82586 2.53125 3.71609 2.55309 3.61369 2.59553C3.51129 2.63796 3.41825 2.70016 3.33989 2.77857H3.34102Z" />
                                    <path fill-rule="evenodd" clip-rule="evenodd"
                                        d="M8.96602 2.77857C8.80801 2.93677 8.71926 3.15123 8.71926 3.37482C8.71926 3.59841 8.80801 3.81287 8.96602 3.97107L13.9936 8.99982L8.96489 14.0286C8.81127 14.1878 8.72632 14.4009 8.72835 14.6222C8.73037 14.8434 8.81921 15.055 8.97572 15.2114C9.13224 15.3677 9.3439 15.4564 9.56513 15.4582C9.78636 15.46 9.99946 15.3748 10.1585 15.2211L15.7835 9.59607C15.9415 9.43787 16.0303 9.22341 16.0303 8.99982C16.0303 8.77623 15.9415 8.56177 15.7835 8.40357L10.1585 2.77857C10.0802 2.70016 9.98712 2.63796 9.88472 2.59553C9.78231 2.55309 9.67255 2.53125 9.5617 2.53125C9.45085 2.53125 9.34109 2.55309 9.23869 2.59553C9.13629 2.63796 9.04325 2.70016 8.96489 2.77857H8.96602Z" />
                                </svg>
                            </button>
                        </div>
                    </div>

                    <div class="content">
                        <h4>{{ item.name }}</h4>

                        <div class="item" v-for="item2 in item.info">
                            <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 20 20" fill="none">
                                <path
                                    d="M19.8288 9.55169L13.8292 2.88538C13.7012 2.74406 13.5225 2.66406 13.3332 2.66406H9.3334C9.20462 2.6642 9.07863 2.70152 8.97054 2.77152C8.86246 2.84153 8.77688 2.94125 8.7241 3.05871C8.61743 3.30003 8.66143 3.58135 8.83742 3.776L14.4358 9.997L8.83742 16.2167C8.66143 16.4127 8.6161 16.694 8.7241 16.934C8.83209 17.1753 9.07074 17.3299 9.3334 17.3299H13.3332C13.5225 17.3299 13.7012 17.2486 13.8292 17.1099L19.8288 10.4436C20.0568 10.1903 20.0568 9.80368 19.8288 9.55169Z"
                                    fill="#143584" />
                                <path
                                    d="M11.1628 9.55169L5.16314 2.88538C5.03514 2.74406 4.85649 2.66406 4.66716 2.66406H0.66738C0.538605 2.6642 0.412609 2.70152 0.304525 2.77152C0.196442 2.84153 0.110867 2.94125 0.0580799 3.05871C-0.048581 3.30003 -0.00458339 3.58135 0.171407 3.776L5.76977 9.997L0.171407 16.2167C-0.00458339 16.4127 -0.0499143 16.694 0.0580799 16.934C0.166074 17.1753 0.404728 17.3299 0.66738 17.3299H4.66716C4.85649 17.3299 5.03514 17.2486 5.16314 17.1099L11.1628 10.4436C11.3908 10.1903 11.3908 9.80368 11.1628 9.55169Z"
                                    fill="#143584" />
                            </svg>
                            <p>{{ item2 }}</p>
                        </div>
                        <p>{{ item.bio }}</p>
                    </div>
                </div>

            </div>
        </div>
    </section>
    <Contact></Contact>
    <Footer></Footer>
</template>
<style scoped>
.team h5 {
    text-align: center;
    color: var(--color-primary);
    margin-bottom: 0.5rem;
}

.team h2 {
    text-align: center;
    margin-top: 0;
    margin-bottom: 2rem;
}

.team .card {
    margin-top: 50px;
}

.team .card h4 {
    border-bottom: 1px solid rgb(221, 221, 221);
    padding-bottom: 0.5em;
    width: max-content;
    font-size: var(--average-font);
}

.team .inner-card {
    display: grid;
    grid-template-columns: 1fr 1fr;
    min-height: 400px;
    gap: 2rem;
}



.team .image-holder {
    position: relative;
    width: 100%;
    height: 560px;
}

.team .image-holder img {
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    border-radius: 8px;
    object-fit: cover;
}

.team .image-holder .outline {
    position: absolute;
    z-index: 2;
    border: 2px solid white;
    left: 12px;
    right: 12px;
    top: 12px;
    bottom: 12px;
    border-radius: 8px;
}

.team .content h4 {
    color: var(--color-primary);
    width: 100%;
    margin: 0;
    margin-bottom: 1.5rem;
}

.team .content .item {
    display: grid;
    grid-template-columns: max-content 1fr;
    align-items: flex-start;
    gap: 1rem;
    margin: 0.5rem 0;
}

.team .content .item svg {
    width: 16px;
}

.team .content .item p {
    margin: 0;
    color: rgb(54, 54, 54);
    font-size: calc(var(--medium-font) + 2px);
    font-weight: bold;
}

.team .button-holder {
    margin-top: 1rem;
    display: flex;
    gap: 1rem;
    justify-content: center;
}

.team .button-holder button {
    padding: 0.5rem;
    border-radius: 0;
}

.team button.left svg {
    rotate: 180deg;
}



@media only screen and (max-width: 700px) {
    .team .inner-card {
        grid-template-columns: 100%;
        gap: 3rem;
    }

    .team .button-holder {
        display: none;
    }

    .team .card>h4 {
        text-align: center;
        margin-left: auto;
        margin-right: auto;
    }

    .team .content h4 {
        width: max-content;
    }

    .team .image-holder {

        height: 400px;
    }
}
</style>