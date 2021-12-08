<template>
    <div>
        <h1>{{ button_message }}</h1>
        <button-one @button_clicked="react_to_button_clicked"></button-one>
        <button-two @button_clicked="react_to_button_clicked"></button-two>
        <button-three @button_clicked="react_to_button_clicked"></button-three>
        <party-button></party-button>
    </div>
</template>

<script>
import ButtonOne from './ButtonOne.vue';
import ButtonTwo from './ButtoneTwo.vue';
import ButtonThree from './ButtonThree.vue';
import PartyButton from './PartyButton.vue';


    export default {
        name: "home_content",
        components: {
            ButtonOne,
            ButtonTwo,
            ButtonThree,
            PartyButton
        },

        data() {
            return {
                button_message: undefined
            }
        },

        methods: {
            react_to_button_clicked(payload) {
                this.button_message = payload;
            }
        },
    }
        
</script>

<style scoped>

</style>