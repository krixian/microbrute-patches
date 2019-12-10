<template>
    <fieldset class="mbp-fieldset">
        <h1 class="mbp-fieldset__heading">
            <span class="mbp-fieldset__heading-text" v-text="label" />
        </h1>

        <mbp-dial />
    </fieldset>
</template>

<script>
import MbpDial from "./MbpDial";
export default {
    components: {
        MbpDial,
    },

    props: {
        label: String,
    }
}
</script>

<style lang="less">
@import (reference) "../styles/variables.less";
@border-radius: .3rem;

.mbp-fieldset {
    background: #2c2c39;
    border: none;
    border-radius: 0 0 @border-radius @border-radius;
    margin: 0;
    padding: 0;

    &__heading {
        background: linear-gradient(to bottom, #fff 0, #fff .4rem, transparent .4rem);
        font-size: @font-size-normal;
        font-weight: @font-weight-normal;
        line-height: 1;
        letter-spacing: .1em;
        margin: 0;
        text-align: center;
        text-transform: uppercase;
    }

    &__heading-text {
        background: #fff;
        border-radius: 0 0 @border-radius @border-radius;
        color: @text-color-dark;
        display: inline-block; 
        padding: .2rem 1.2rem;
    }
}
</style>