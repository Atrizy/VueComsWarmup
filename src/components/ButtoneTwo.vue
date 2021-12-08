<template>
    <div>
        <button @click="button_clicked" ref="btn">Button Two</button>
    </div>
</template>

<script>
    export default {
        name: 'button_two',
        methods: {
            button_clicked() {
                this.$emit('button_clicked', 'Button Two Clicked!');
                this.$refs['btn'].style.background = "orange";
            },
            
            party_time() {
                this.$refs['btn'].innerText = "Button Two Party Time!"
            }
        },
        mounted () {
            this.$root.$on('party_time', this.party_time);
        },
    }

</script>

<style scoped>

</style>