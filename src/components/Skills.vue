<template>
    <div class="skills-page column">
        <div class="txt">
            <p class="gradient">As I said before, I am currently in my second year of study in web development, so this page is bound to grow.</p>
        </div>
        <div class="container-skills">
            <h2 class="gradient">Front-end.</h2>
            <div class="skills flex-wrap">
                <div v-for="front in fronts" :key="front" class="skill center-total">
                    <img v-bind:src="front.image"  alt="skill">
                </div>
            </div>
        </div>
        <div class="container-skills">
            <h2 class="gradient">Back-end.</h2>
            <div class="skills flex-wrap">
                <div v-for="back in backs" :key="back" class="skill center-total">
                    <img v-bind:src="back.image"  alt="skill">
                </div>
            </div>
        </div>
        <div class="container-skills">
            <h2 class="gradient">Ui design.</h2>
            <div class="skills flex-wrap">
                <div v-for="ui in uis" :key="ui" class="skill center-total">
                    <img v-bind:src="ui.image"  alt="skill">
                </div>
            </div>        
        </div>
    </div>
</template>

<script>
export default {
    name: 'Skills',
    data() {
        return {
            fronts:[
                {image: require('@/assets/tech/html.png')},
                {image: require('@/assets/tech/css.png')},
                {image: require('@/assets/tech/javascript-fill.png')},
                {image: require('@/assets/tech/vuejs.png')},
                {image: require('@/assets/tech/tailwind.png')},
                {image: require('@/assets/tech/sass.png')},
                {image: require('@/assets/tech/angular.png')}
            ],
            backs:[
                {image: require('@/assets/tech/php.png')},
                {image: require('@/assets/tech/mysql.png')},
                {image: require('@/assets/tech/symfony.png')},
                {image: require('@/assets/tech/laravel.png')},
                {image: require('@/assets/tech/python-fill.png')},
                {image: require('@/assets/tech/wordpress.png')},
                {image: require('@/assets/tech/shopify.png')}
            ],
            uis: [
                {image: require('@/assets/tech/adobe-xd.png')},
                {image: require('@/assets/tech/figma.png')}
            ]
        }
    },
}
</script>

<style lang="scss">
    .skills-page {
        margin: 0 auto;
        padding: 1rem;
        width: 80%;
        gap: 60px;
        .txt {
            margin: 0 auto;
            margin: 30px;
            p {
                text-align: center;
            }
        }
        .skills, h2 {
            margin-bottom: 20px;
        }
    }
    .container-skills {
        margin: 0 auto;
    }
    .skills {
        gap: 28px;
    }
    .skill {
        cursor: pointer;
        padding: 1rem;
        width: 100px;
        height: 100px;
        background: var(--bgContainer);
        border-radius: 20px;
        img {
            width: 60px;
            height: auto;
        }
        &:hover {
            transition: ease 0.3s;
            transform: scale(1.1);
            box-shadow: 0px 2px 8px 0px #00000040;
        }
    }
    #figma-logo {
        width: 49px;
        height: 69px;
    }
</style>