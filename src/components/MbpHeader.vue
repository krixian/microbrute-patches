<template>
    <header class="mbp-header">
        <h1 class="mbp-header__title">
            Micro<span class="mbp-header__strong">Brute</span>
        </h1>
        <p class="mbp-header__sub-title">Patch Configuration</p>
    </header>
</template>

<style lang="less">
@import (reference) "../styles/variables.less";

.mbp-header {
    color: #fff;
    display: inline-block;
    margin: 1rem 0;
    text-transform: uppercase;

    &__title {
        font-size: @font-size-title;
        font-weight: @font-weight-normal;
        line-height: 1;
        margin: 0;
    }

    &__strong {
        font-weight: @font-weight-bold;
    }

    &__sub-title {
        font-size: @font-size-small;
        font-weight: @font-weight-normal;
        line-height: 1;
        text-align: end;
        margin: 0;
    }
}
</style>