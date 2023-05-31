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


    </footer>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;

footer {
    background-image: url("../assets/img/footer-bg.jpg");
    padding: 50px 0;


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
</style>