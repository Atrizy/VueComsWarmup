<template>
    <div>
        <button @click="button_clicked" ref="btn">Button Three</button>
    </div>
</template>

<script>
    export default {
        name: 'button_three',
        methods: {
            button_clicked() {
                this.$emit('button_clicked', 'Button Three Clicked!');
                this.$refs['btn'].style.background = "orange";
            },
            
            party_time() {
                this.$refs['btn'].innerText = "Button Three Party Time!"
            }
        },
        mounted () {
            this.$root.$on('party_time', this.party_time);
        },
    }

</script>

<style scoped>

</style>