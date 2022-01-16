<template>
    <div class="container center-total">
        <div class="txt column center-total">
            <p class="gradient">My projects presented on this page are almost all deposited on my github. If you wish, you can consult it!</p>
            <img class="arrow" src="@/assets/logos/arrow-down.png" alt="arrow">
            <div class="button center-total">
                <a href="https://github.com/ClemOurs" target="_blank">my github page</a>
            </div>
        </div>
        <div class="container-project">
            <div v-for="project in projects" :key="project" class="box">
                <div class="content">
                    <h2>{{project.name}}</h2>
                    <small>{{project.subtitle}}</small>
                    <p>{{project.description}}</p>
                    <div class="languages flex-wrap">
                        <img v-for="lang in project.languages" :key="lang" :src="lang" alt="language">
                    </div>
                </div>
                <div class="images">
                    <img v-for="image in project.images" :key="image" :src="image" alt="project image">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'Projects',
        data() {
            return {
                projects: [
                    {
                        name: 'Ben Solo',
                        subtitle: 'SCHOOL YEAR PROJECT',
                        description: 'the goal of this project was to make us learn the basics of development, on a subject of our choice.',
                        languages: [
                            require('@/assets/tech/html.png'), 
                            require('@/assets/tech/css.png'), 
                            require('@/assets/tech/javascript-fill.png'), 
                            require('@/assets/tech/php.png'), 
                            require('@/assets/tech/mysql.png')
                        ],
                        images: [
                            require('@/assets/screens_projects/bensolo/presentation.png'),
                            require('@/assets/screens_projects/bensolo/galerie.png'),
                            require('@/assets/screens_projects/bensolo/home.png'),
                        ]
                    },
                    {
                        name: 'Jadoo',
                        subtitle: 'SASS PROJECT',
                        description: 'the goal of this project was to make us learn the basics of sass, with a template to reproduce.',
                        languages: [
                            require('@/assets/tech/html.png'), 
                            require('@/assets/tech/css.png'), 
                            require('@/assets/tech/javascript-fill.png'), 
                            require('@/assets/tech/php.png'), 
                            require('@/assets/tech/mysql.png')
                        ],
                        images: [
                            require('@/assets/screens_projects/maquette/footer.png'),
                            require('@/assets/screens_projects/maquette/destinations.png'),
                            require('@/assets/screens_projects/maquette/header.png'),
                        ]
                    },
                    {
                        name: 'Ping Passion',
                        subtitle: 'WORDPRESS PROJECT',
                        description: 'the goal of this project was to make us learn the basics of wordpress.',
                        languages: [
                            require('@/assets/tech/html.png'), 
                            require('@/assets/tech/css.png'), 
                            require('@/assets/tech/javascript-fill.png'), 
                            require('@/assets/tech/php.png'), 
                            require('@/assets/tech/mysql.png')
                        ],
                        images: [
                            require('@/assets/screens_projects/wordpress/home.png'),
                            require('@/assets/screens_projects/wordpress/revetements.png'),
                            require('@/assets/screens_projects/wordpress/bois.png'),
                        ]
                    }
                ]
            }
        },
    }
</script>

<style lang="scss">
    .container {
        flex-direction: column;
        .txt {
            margin: 0 auto;
            gap: 15px;
            padding: 1rem;
            width: 80%;
            p {
                text-align: center;
            }
        }
        
        .box {
            padding: 1rem 3rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            min-height: 100px;
            background-color: var(--bgContainer);
            margin: 20px;
            margin-bottom: 30px;
            border-radius: 10px;
            box-shadow: 0px 2px 8px 0px #00000040;

            .content {
                padding: 1rem;
                width: 100%;
                line-height: 25px;

                h2 {
                    font-size: 2.5rem;
                    font-weight: bold;
                    margin-bottom: 20px;
                }

                p {
                    font-size: 1rem;
                    margin-top: 20px;
                }

                .languages {
                    padding: 1rem;
                    align-items: center;

                    img {
                        width: 30px;
                        height: fit-content;
                        margin-right: 15px;
                    }
                }
            }

            .images {
                position: relative;
                width: 100%;
                height: 350px;
                img {
                    border-radius: 10px;
                    position: absolute;
                    width: 300px;
                    height: auto;
                    object-fit: cover;

                    &:nth-child(1) {
                        left: 100px;
                        top: 50px;
                    }
                    &:nth-child(2) {
                        left: 150px;
                        top: 100px;
                    }
                    &:nth-child(3) {
                        left: 200px;
                        top: 150px;
                    }
                }
            }
        }
    }
    @media screen and (max-width: 1400px) {
        .container {
            .box {
                width: 90vw;
                display: flex;
                flex-direction: column;
                text-align: center;

                .content {
                    .languages {
                        justify-content: center;
                    }
                }

                .images {
                    position: initial;
                    display: flex;
                    flex-wrap: wrap;
                    width: 100%;
                    height: auto;
                    margin: 0 auto;
                    img {
                        width: 30%;
                        display: flex;
                        justify-content: center;
                        align-items: center;
                        margin: 10px auto;
                        height: auto;
                        position: initial;
                    }
                }

            }
        }
    }

    @media screen and (max-width: 900px) {
        .container {
            .box {
                .images {
                    img {
                        width: 90%;
                    }
                }
                .content {
                    h2 {
                        font-size: 1.5rem;
                    }
                }
            }
        }
        .languages {
            img {
                width: 30px;
                height: 30px;
            }
        }
    }
</style>