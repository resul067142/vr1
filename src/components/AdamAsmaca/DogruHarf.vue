<template>
    <div>
        <h3>Kelime</h3>
        {{word}}
        {{letter}}
        <ul>
            <li v-for="(letter, index) in word.split('')" :key="index">{{letter}}</li>
        </ul>
    </div>
</template>

<script>
export default {
    props: ["word", "letter"]
}
</script>

<style lang="scss" scoped>

ul {
    list-style: none;
    li {
        display: inline-block;
        padding: 1rem;
        margin-right: 1rem;
        border-bottom: 3px solid red;

        &.active {
            border-color: green;
        }
    }
}

</style>