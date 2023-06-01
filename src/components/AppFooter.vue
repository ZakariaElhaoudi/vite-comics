<script>
export default {
    name: 'AppFooter',
    data() {
        return {
            links: [
                {
                    link: '#',
                    text: 'Characters',
                    status: false
                },
                {
                    link: '#',
                    text: 'Comics',
                    status: true
                },
                {
                    link: '#',
                    text: 'Movies',
                    status: false
                },
                {
                    link: '#',
                    text: 'TV',
                    status: false
                },
                {
                    link: '#',
                    text: 'Games',
                    status: false
                },
                {
                    link: '#',
                    text: 'Videos',
                    status: false
                },
                {
                    link: '#',
                    text: 'News',
                    status: false
                },
            ]

        }
    }
}
</script>

<template>
    <footer>
        <div class="container">
            <div class="container">
                <div>
                    <nav>
                        <h2>DC COMICS</h2>
                        <ul>
                            <li v-for="link in links" :class="link.status ? 'active' : ''">
                                <a :href="link.link">{{ link.text }}</a>
                            </li>
                        </ul>
                    </nav>
                    <nav>
                        <h2>SHOP</h2>
                        <ul>
                            <li><a href="#">Shop DC</a></li>
                            <li><a href="#">Shop DC Collectibles</a></li>
                        </ul>
                    </nav>
                </div>
                <div>
                    <nav>
                        <h2>DC</h2>
                        <ul>
                            <li><a href="#">Shop DC</a></li>
                            <li><a href="#">Shop DC Collectibles</a></li>
                            <li><a href="#">Shop DC</a></li>
                            <li><a href="#">Shop DC Collectibles</a></li>
                            <li><a href="#">Shop DC</a></li>
                            <li><a href="#">Shop DC Collectibles</a></li>
                            <li><a href="#">Shop DC</a></li>
                            <li><a href="#">Shop DC Collectibles</a></li>
                            <li><a href="#">Shop DC</a></li>
                            <li><a href="#">Shop DC Collectibles</a></li>
                            <li><a href="#">Shop DC</a></li>
                        </ul>
                    </nav>
                </div>
                <div>
                    <nav>
                        <h2>SITES</h2>
                        <ul>
                            <li><a href="#">Shop DC</a></li>
                            <li><a href="#">Shop DC Collectibles</a></li>
                            <li><a href="#">Shop DC</a></li>
                            <li><a href="#">Shop DC Collectibles</a></li>
                            <li><a href="#">Shop DC</a></li>
                        </ul>
                    </nav>
                </div>
            </div>
            <div class="logo-footer">
                <img src="../assets/img/dc-logo-bg.png" alt="">
            </div>
        </div>

        <section>
            <div class="container buttom">
                <button>
                    SIGN-UP NOW!
                </button>
                <div class="follow">
                    <div class="text">
                        FOLLOW US
                    </div>
                    <div class="icon">
                        <div class="image">
                            <a href="#"><img src="../assets/img/footer-facebook.png" alt="logo facebook"></a>
                        </div>
                        <div class="image">
                            <a href="#"><img src="../assets/img/footer-twitter.png" alt="logo twitter"></a>
                        </div>
                        <div class="image">
                            <a href="#"><img src="../assets/img/footer-youtube.png" alt="logo youtube"></a>
                        </div>
                        <div class="image">
                            <a href="#"><img src="../assets/img/footer-periscope.png" alt="logo pinterest"></a>
                        </div>
                        <div class="image">
                            <a href="#"><img src="../assets/img/footer-pinterest.png" alt="logo periscope"></a>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </footer>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;
@use '../styles/partials/variables.scss' as *;

footer {
    background-image: url("../assets/img/footer-bg.jpg");
    padding-top: 20px;

    section {
        background-color: black;
        height: 90px;

        .container.buttom {
            height: 90px;
            display: flex;
            justify-content: space-between;
            align-items: center;

            .icon {
                display: flex;

                .image {
                    width: 25px;
                    margin-inline: 5px;
                }
            }

            .follow {
                display: flex;
                align-items: center;

                .text {
                    color: $primary;
                    margin-right: 10px;
                    font-weight: 600;
                }
            }

            button {
                background-color: black;
                border: 2px solid $primary;
                padding: 10px;
                color: white;
            }
        }
    }

    .container {
        display: flex;

        h2 {
            color: white;
            padding-left: 2rem;
        }

        ul {
            margin: 1rem 1rem 1rem;


            li a {
                text-decoration: none;
                padding: 1rem;
                font-weight: 600;
                transition: background 0.3s;
                color: gray;

                &:hover {
                    color: $primary;
                }
            }
        }
    }
}

.logo-footer {
    position: relative;
    top: -20px;
    width: 450px;
}
</style>