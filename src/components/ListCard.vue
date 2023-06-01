<script>
export default {
    name: 'ListCard',
    props: {
        card: Object,
    }

}
</script>

<template>
    <div class="card">
        <a href="#"><img :src="card.thumb" :alt="card.series"></a>
        <a href="#">
            <h3>{{ card.series }}</h3>
        </a>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;

.card {
    width: calc(100% / 6 - 20px);
    margin: 0 10px;
    padding-bottom: 60px;
    height: 250px;


    a {
        color: white;

        &:hover {
            color: $primary;
        }

        img {
            max-height: 100%;
        }
    }

}
</style>