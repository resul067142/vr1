<template>
    <div>
        <h3>Hatalı Harf</h3>
        <div>
            a,b,c
        </div>
    </div>
</template>

<script>
export default {
    props: ["word", "letter"],
    data() {
        return {}
    },
    watch: {
        letter(val) {
            console.log("Hatali harf",val);
            if (this.word.split('').indexOf(val) > 0) {
                console.log(this.word.split('').indexOf(val));
            }
        },
    }
}
</script>