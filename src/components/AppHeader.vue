<script>
export default {
    name: 'AppHeader',
    data() {
        return {
            links: [
                {
                    link: '#',
                    text: 'CHARACTERS',
                    status: false
                },
                {
                    link: '#',
                    text: 'COMICS',
                    status: true
                },
                {
                    link: '#',
                    text: 'MOVIES',
                    status: false
                },
                {
                    link: '#',
                    text: 'TV',
                    status: false
                },
                {
                    link: '#',
                    text: 'GAMES',
                    status: false
                },
                {
                    link: '#',
                    text: 'COLLECTIBLES',
                    status: false
                },
                {
                    link: '#',
                    text: 'VIDEOS',
                    status: false
                },
                {
                    link: '#',
                    text: 'FANS',
                    status: false
                },
                {
                    link: '#',
                    text: 'NEWS',
                    status: false
                },
                {
                    link: '#',
                    text: 'SHOP',
                    status: false
                },
            ]
        }
    }
}
</script>

<template>
    <header>
        <a href="#">
            <img src="../assets/img/dc-logo.png" class="logo" alt="DC logo" />
        </a>

        <nav>
            <ul>
                <li v-for="link in links" :class="status ? 'active' : ''">
                    <a :href="link.link">{{ link.text }}</a>

                </li>
            </ul>
        </nav>
    </header>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;

header {
    width: 80%;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;

    ul {
        display: flex;
        align-items: center;
        margin: 2.5rem 1rem 4rem;

        li {
            list-style: none;

            a {
                display: inline-block;
                text-decoration: none;
                padding: 1rem;
                font-weight: 600;
                transition: background 0.3s;

                &.active,
                &:hover {
                    color: $primary;
                    padding-bottom: 1em;
                    border-bottom: solid 2px $primary ;
                }
            }
        }
    }

}
</style>