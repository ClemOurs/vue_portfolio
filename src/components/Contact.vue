<template>
    <div class="contact-header column">
        <h1 class="gradient">Contact me.</h1>
        <p>Do not hesitate to contact me, I will answer you as soon as possible !</p>
    </div>
    <div class="infos flex-wrap">
        <div class="reach column">
            <div class="container-info contact">
                <h5>by email.</h5>
                <div class="email button row center-total">
                    <img src="@/assets/logos/mail.png" alt="mail">
                    <p>duvivier.clem@gmail.com</p>
                </div>
            </div>
            <div class="container-info contact">
                <h5>by phone.</h5>
                <div class="row center-total">
                    <img src="@/assets/logos/phone.png" alt="phone">
                    <p>+33.6.83.70.18.85</p>
                </div>
            </div>
        </div>
        <div class="container-info-socials contact">
            <h5>by socials.</h5>
            <div class="row">
                <img src="@/assets/logos/linkedin-fill.png" alt="social">
                <p>Clément Duvivier</p>
            </div>
            <div class="row">
                <img src="@/assets/logos/github.png" alt="social">
                <p>ClemOurs</p>
            </div>
        </div>
    </div>
</template>

<style lang="scss">
    .contact-header {
        display: flex;
        align-items: center;
        margin-bottom: 50px;
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
        gap: 21px;
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