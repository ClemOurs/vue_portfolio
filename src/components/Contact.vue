<template>
    <div class="contact-page">
        <div class="contact-header column">
            <h1 class="gradient">Contact me.</h1>
            <p>Do not hesitate to contact me, I will answer you as soon as possible !</p>
        </div>
        <div class="infos flex-wrap">
            <div class="reach column">
                <div class="container-info contact">
                    <h5>by email.</h5>
                    <div class="email row info">
                        <img src="@/assets/logos/mail.png" alt="mail">
                        <p class="gradient">duvivier.clem@gmail.com</p>
                    </div>
                </div>
                <div class="container-info contact">
                    <h5>by phone.</h5>
                    <div class="row info">
                        <img src="@/assets/logos/phone.png" alt="phone">
                        <p class="gradient">+33.6.83.70.18.85</p>
                    </div>
                </div>
            </div>
            <div class="container-info-socials contact">
                <h5>by socials.</h5>
                <div class="row">
                    <img src="@/assets/logos/linkedin-fill.png" alt="social">
                    <a class="gradient" href="https://www.linkedin.com/in/clementduvivier/">Clément Duvivier</a>
                </div>
                <div class="row">
                    <img src="@/assets/logos/github.png" alt="social">
                    <a class="gradient" href="https://github.com/ClemOurs">ClemOurs</a>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss">
    .contact-page {
        height: 100vh;
    }
    .contact-header {
        display: flex;
        gap: 20px;
        align-items: center;
        margin: 70px;
        p {
            text-align: center;
        }
    }
    .infos {
        justify-content: center;
        gap: 35px;
        h5 {
            font-weight: 500;
            margin-bottom: 20px;
        }
    }
    .reach {
        width: 300px;
        min-height: 100px;
        gap: 21px;
    }
    .info {
        align-items: center;
    }
    .container-info {
        padding: 15px;
        border-radius: 20px;
        .row {
            padding: 10px;
            gap: 5px;
        }
        &-socials {
            padding: 2rem;
            border-radius: 20px;
            .row {
                padding: 0;
                gap: 13px;
                align-items: center;
                margin-bottom: 18px;
            }
        }
        .email {
            height: 30px;
        }
    }
    .contact {
        background-color: var(--bgContainer);
        box-shadow: 0px 2px 8px 0px #00000040;
        .row {
            img {
                width: 30px;
                height: 30px;
            }
        }
    }
</style>