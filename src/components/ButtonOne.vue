<template>
    <div>
        <button @click='button_clicked' ref="btn">Button One</button>
    </div>
</template>

<script>
    export default {
        name: 'button_one',
        methods: {
            button_clicked() {
                this.$emit('button_clicked', 'Button One Clicked!');
                this.$refs['btn'].style.background = "orange";
            },
            
            party_time() {
                this.$refs['btn'].innerText = "Button One Party Time!"
            }
        },
        mounted () {
            this.$root.$on('party_time', this.party_time);
        },
    }
</script>

<style scoped>

</style>