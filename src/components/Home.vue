<template>
    <div class="header-container column center-total">
        <h1 class="gradient">Hi, I'm Clément Duvivier.</h1>
        <div class="find-me row center">
            <img id="location" src="@/assets/logos/location.png" alt="location">
            <p id="city">Paris, France</p>
        </div>
        <div class="txt center-total">
            <p>I’m currently studying at IIM Digital School in Nanterre, to become a fullstack developper.</p>
            <p id="search">Right now, I'm looking for an internship for a period of 3 months from May to August as well as a work-study program for my third year.</p>
            <div class="margin">
                <img class="arrow" src="@/assets/logos/arrow-down.png" alt="arrow">
            </div>
            <div class="button row center-total">
                <p>Learn more </p>
                <a href="#">about me.</a>
            </div>
        </div>
    </div>
    <section class="journey">
        <h2 class="gradient">My journey.</h2>
        <div class="txt">
            <p>Passionate about many different fields I had previously started studying networks and telecoms, however I soon realized that it was only going to remain a distant passion...</p>
            <p>So I decided to go back to IIM, a school that I had already spotted at the end of my high school period.</p>
            <p>Currently in my second year of bachelor and I’m studying web development !</p>
            <div class="center-total">
                <img class="arrow" src="@/assets/logos/arrow-down.png" alt="arrow">
            </div>
            <div class="button learn-more center-total">
                <a href="#">learn more about my experience</a>
            </div>
        </div>
    </section>
</template>
<script>
</script>
<style lang="scss">
    .header-container {
        background-image: url("../assets/bg_header.png");
        background-repeat: no-repeat;
        background-position: fixed;
        background-size: cover;
        width: 80%;
        height: 60vh;
        margin: 0 auto;
        .find-me {
            gap: 10px;
        }
        .txt {
            width: 80%;
            flex-direction: column;
            #search {
                text-align: justify;
                width: 60%;
                margin-top: 30px;
            }
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
        font-size: 60px;
    }
    .row {
        padding: 1rem;
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
    .journey {
        margin: 0 auto;
        width: 60%;
        border-radius: 30px 30px 0 0;
        padding: 1rem;
        background-color: var(--bgContainer);
        h2 {
            padding: 10px;
            font-weight: bold;
            margin-bottom: 20px;
        }
        .txt {
            margin: 0 auto;
            width: 70%;
            p {
                font-size: 14px;
                margin-bottom: 30px;
            }
        }
        .learn-more {
            margin-bottom: 75px;
        }
    }
</style>