<template>
    <div class="header-container column center-total">
        <h1 class="gradient">Hi, I'm Clément Duvivier.</h1>
        <div class="find-me row center">
            <img id="location" src="@/assets/logos/location.png" alt="location">
            <p id="city">Paris, France</p>
        </div>
        <div class="txt center-total">
            <p>I’m currently studying at IIM Digital School in Nanterre, to become a fullstack developper.</p>
            <p>Right now, I'm looking for an internship for a period of 3 months from May to August as well as a work-study program for my third year.</p>
            <div class="margin">
                <img class="arrow" src="@/assets/logos/arrow-down.png" alt="arrow">
            </div>
            <div class="button row center-total">
                <p>Learn more </p>
                <a href="#" target="_blank">about me.</a>
            </div>
        </div>
    </div>
    <section class="about-me">
        <h2 class="gradient">My journey.</h2>
        <div class="txt">
            <p>Passionate about many different fields I had previously started studying networks and telecoms, however I soon realized that it was only going to remain a distant passion...</p>
            <p>So I decided to go back to IIM, a school that I had already spotted at the end of my high school period.</p>
            <p>Currently in my second year of bachelor and I’m studying web development !</p>
        </div>
        <h2 class="gradient">My passions.</h2>
        <ul class="cards flex-wrap">
            <li class="card" v-for="passion in passions" :key="passion.id">
                <img v-bind:src="passion.image" alt="passion"/>
                <div class="passion center-total">
                    <h5 class="title-passion">{{passion.name}}.</h5>
                </div>
            </li>
        </ul>
    </section>
</template>

<script>
export default {
    data() {
        return {
            passions: [
                {id: 0, name: "Video Games", image: require("@/assets/passions/videogame.jpeg")},
                {id: 1, name: "Cinema", image: require("@/assets/passions/cinema.jpeg")},
                {id: 2, name: "Photography", image: require("@/assets/passions/photography.jpeg")},
                {id: 3, name: "Code", image: require("@/assets/passions/code.jpeg")},
                {id: 4, name: "Trips", image: require("@/assets/passions/trip.jpeg")},
                {id: 5, name: "Music", image: require("@/assets/passions/music.jpeg")},
            ]
        }
    },
}
</script>

<style lang="scss">
    .header-container {
        padding: 1rem;
        background-image: url("../assets/bg_header.png");
        background-repeat: no-repeat;
        background-position: fixed;
        background-size: cover;
        gap: 30px;
        width: 80%;
        height: 60vh;
        margin: 0 auto;
        .find-me {
            gap: 10px;
        }
        .txt {
            padding: 1rem;
            width: 50%;
            text-align: justify;
            flex-direction: column;
            gap: 19px;
            a:hover {
                color: var(--blue);
                text-decoration: underline;
            }
            .button {
                gap: 5px;
            }
            .margin {
                margin-top: 15px;
            }
        }
        margin-bottom: 30px;
    }
    h1 {
        font-size: 80px;
    }
    .row {
        display: flex;
        flex-direction: row;
        &.center {
            align-items: center;
        }
    }
    #city {
        font-size: 18px;
        font-weight: bold;
    }
    #location {
        width: 30px;
        height: 30px;
    }
    .about-me {
        margin: 0 auto;
        width: 60%;
        border-radius: 30px 30px 0 0;
        padding: 1rem;
        background-color: var(--bgContainer);
        h2 {
            display: flex;
            justify-content: center;
            padding: 10px;
            font-weight: bold;
            margin-bottom: 20px;
        }
        .txt {
            margin: 0 auto;
            width: 60%;
            text-align: justify;
            p {
                font-size: 18px;
                margin-bottom: 30px;
            }
        }
        .learn-more {
            margin-bottom: 75px;
        }
    }
    .cards {
        padding: 1rem;
        justify-content: center;
        gap: 30px;
        .card {
            cursor: pointer;
            position: relative;
            .passion {
                transition: 0.3s ease;
                opacity: 0;
                position: absolute;
                top: 0;
                left: 0;
                width: 100%;
                height: 98%;    
                background: var(--gradient);
                border-radius: 10px;
            }
            img {
                border-radius: 10px;
                width: 350px;
                height: 200px;
                &:hover {
                    opacity: 0.3;
                    transition: 0.3s;
                }
            }
            &:hover .passion {
                opacity: 1;
            }
        }
    }
    .title-passion {
        color: var(--white);
        text-transform: lowercase;
        font-weight: bold;
    }
    @media screen and (max-width: 1300px) {
        .header-container {
            .txt {
                width: 80%;
            }
        }
        .about-me {
            width: 90%;
        }
    }
    @media screen and (max-width: 900px) {
        .header-container {
            gap: 20px;
            width: 100%;
            h1 {
                font-size: 30px;
            }
            .txt {
                width: 90%;
            }
        }
        .about-me {
            .gradient {
                color: #000;
            }
            .txt {
                width: 90%;
            }
        }
    }
</style>