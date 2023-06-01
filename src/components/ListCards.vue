<script>
export default {
    name: 'ListCards',

    props: {
        cards: Array,
    }

}
</script>

<template>
    <div class="card" v-for="card in cards">
        <img :src="card.thumb" :alt="card.series">
        <h3>{{ card.series }}</h3>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;

.card {
    width: calc(100% / 6);
    height: 60px;
}
</style>