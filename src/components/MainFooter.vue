<template>
    <footer class="row">
        <div class="footer-content column">
            <div class="logos row">
                <a href="https://www.linkedin.com/in/clementduvivier/" target="_blank"><img src="../assets/logos/linkedin-fill-white.png" alt="logo"></a>
                <a href="https://github.com/ClemOurs" target="_blank"><img src="../assets/logos/github-white.png" alt="logo"></a>
                <img src="../assets/logos/abattu.png" alt="logo">
            </div>
            <p id="copyrights">© 2022 | Clément Duvivier | All rights reserved.</p>
            <ul class="links row">
                <li><a href="#">Home</a></li>
                <li><a href="#">Skills</a></li>
                <li><a href="#">Projects</a></li>
                <li><a href="#">Experience</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </div>
        <img src="../assets/memoji/memoji_2.png" alt="memoji">
    </footer>
</template>

<script>
</script>

<style lang="scss">
    footer {
        position: fixed;
        bottom: 0;
        width: 100%;
        align-items: center;
        justify-content: space-around;
        background-color: var(--bgFooter);
        height: 200px;
        .links, .logos {
            gap: 20px;
        }
        img {
            width: 75px;
            height: 112px;
        }
    }
    .footer-content {
        gap: 10px;
        a, p {
            font-size: 12px;
            color: var(--grey);
        }
        a:hover {
            transition: ease 0.3s;
            text-decoration: underline;
        }
    }
    .logos {
        img {
            width: 30px;
            height: 30px;
        }
    }
</style>