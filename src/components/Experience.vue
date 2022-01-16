<template>
    <div class="txt dd-container column center-total">
        <p class="gradient">feel free to download my resume right here.</p>
        <img class="arrow" src="@/assets/logos/arrow-down.png" alt="arrow">
        <a class="button resume center-total" href="@/assets/mon_cv.pdf" download="cv_clement_duvivier">my resume.</a>
    </div>
    <div class="container experiences column">
        <div v-for="experience in experiences" :key="experience" class="block row">
            <img class="logo-experience" v-bind:src="experience.logo" alt="logo">
            <div class="txt-experience column">
                <p>{{experience.duration}}</p>
                <h3>{{experience.title}}</h3>
                <h5>{{experience.name}}</h5>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Experience',
    data() {
        return {
            experiences: [
                {
                    name: '404 DeVinci',
                    duration: 'October 2021 - 202X',
                    title: 'Co-Head Events',
                    logo: require('@/assets/experiences/La404_logo_couleur.png'),
                },
                {
                    name: 'HSBC',
                    duration: 'August 2021',
                    title: 'Summer job',
                    logo: require('@/assets/experiences/hsbc.png'),
                },
                {
                    name: 'Mihy',
                    duration: 'June 2021 - July 2021',
                    title: 'Intern front-end developper',
                    logo: require('@/assets/experiences/mihy.png'),
                },
                {
                    name: 'Orange',
                    duration: 'September 2019 - June 2020',
                    title: 'Apprentice',
                    logo: require('@/assets/experiences/orange.png'),
                },
            ]
        }
    },
}
</script>

<style lang="scss">
    .dd-container {
        gap: 15px;
        margin: 35px;
    }
    .experiences {
        align-items: center;
    }
    .logo-experience {
        width: 130px;
    }
    .resume {
        height: 30px;
    }
    .block {
        width: 70%;
        padding: 1rem 3rem;
        gap: 30px;
        display: flex;
        align-items: center;
        min-height: 150px;
        background-color: var(--bgContainer);
        margin: 20px;
        border-radius: 10px;
        &:hover {
            transition: ease 0.3s;
            transform: scale(1.2);
            box-shadow: 0px 2px 8px 0px #00000040;
        }
    }
    .txt-experience {
        width: max-content;
    }
    @media screen and (max-width: 900px) {
        .block {
            display: flex;
            flex-direction: column;
            text-align: center;
        }
    }
</style>