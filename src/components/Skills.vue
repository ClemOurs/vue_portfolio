<template>
    <div class="skills-page center-total">
        <div class="txt">
            <p>As I said before, I am currently in my second year of study in web development, so this page is bound to grow.</p>
        </div>
        <div class="container-skills">
            <h2 class="gradient">Front-end.</h2>
            <div class="skills flex-wrap">
                <div class="skill center-total">
                    <img src="@/assets/tech/html.png" alt="skill front">
                </div>
                <div class="skill center-total">
                    <img src="@/assets/tech/css.png" alt="skill front">
                </div>
                <div class="skill center-total">
                    <img src="@/assets/tech/javascript-fill.png" alt="skill front">
                </div>
                <div class="skill center-total">
                    <img src="@/assets/tech/vuejs.png" alt="skill front">
                </div>
                <div class="skill center-total">
                    <img src="@/assets/tech/tailwind.png" alt="skill front">
                </div>
                <div class="skill center-total">
                    <img src="@/assets/tech/sass.png" alt="skill front">
                </div>
                <div class="skill center-total">
                    <img src="@/assets/tech/angular.png" alt="skill front">
                </div>
            </div>
        </div>
        <div class="container-skills">
            <h2 class="gradient">Back-end.</h2>
            <div class="skills flex-wrap">
                <div class="skill center-total">
                    <img src="@/assets/tech/php.png" alt="skill back">
                </div>
                <div class="skill center-total">
                    <img src="@/assets/tech/mysql.png" alt="skill back">
                </div>
                <div class="skill center-total">
                    <img src="@/assets/tech/symfony.png" alt="skill back">
                </div>
                <div class="skill center-total">
                    <img src="@/assets/tech/laravel.png" alt="skill back">
                </div>
                <div class="skill center-total">
                    <img src="@/assets/tech/python-fill.png" alt="skill back">
                </div>
                <div class="skill center-total">
                    <img src="@/assets/tech/wordpress.png" alt="skill back">
                </div>
                <div class="skill center-total">
                    <img src="@/assets/tech/shopify.png" alt="skill back">
                </div>
            </div>
        </div>
        <div class="container-skills">
            <h2 class="gradient">Ui design.</h2>
            <div class="skills flex-wrap">
                <div class="skill center-total">
                    <img src="@/assets/tech/adobe-xd.png" alt="skill UI">
                </div>
                <div class="skill center-total">
                    <img id="figma-logo" src="@/assets/tech/figma.png" alt="skill UI">
                </div>
            </div>        
        </div>
    </div>
</template>

<style lang="scss">
    .skills-page {
        flex-direction: column;
        height: 100vh;
        .txt {
            width: 50%;
            text-align: justify;
            margin-bottom: 30px;
        }
        .skills, h2 {
            margin-bottom: 20px;
        }
    }
    .skills {
        width: 500px;
        gap: 28px;
    }
    .skill {
        padding: 1rem;
        width: 100px;
        height: 100px;
        background: var(--bgContainer);
        border-radius: 20px;
        img {
            width: 60px;
            height: auto;
        }
    }
    #figma-logo {
        width: 49px;
        height: 69px;
    }
</style>