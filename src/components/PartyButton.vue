<template>
    <div>
        <button @click="party_time">PARY TIME!!!!</button>
    </div>
</template>

<script>
    export default {
        name: "party_button",
        methods: {
            party_time() {
                this.$root.$emit('party_time', 'PARTY IS NOW!')
            }
        },
    }
</script>

<style lang="scss" scoped>

</style>