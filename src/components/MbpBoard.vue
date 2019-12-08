<template>
    <form class="mcp-board">
        <mbp-fieldset class="mcp-board__oscillator" label="Oscillator" />
        <mbp-fieldset class="mcp-board__filter" label="Filter" />
        <mbp-fieldset class="mcp-board__mod-matrix" label="Mod Matrix" />
        <mbp-fieldset class="mcp-board__controls" label="Controls" />
        <mbp-fieldset class="mcp-board__lfo" label="LFO" />
        <mbp-fieldset class="mcp-board__envelope" label="Envelope" />
        <mbp-fieldset class="mcp-board__sequencer" label="Sequencer" />
    </form>
</template>

<script>
import MbpFieldset from './MbpFieldset.vue';

export default { 
    components: {
        MbpFieldset,
    }
}
</script>

<style lang="less">
.mcp-board {
    display: grid;
    grid-template: 10fr 9fr / 1fr 1fr 1fr 1fr 1fr 1fr 1fr 1fr 1fr;
    grid-gap: 1rem;
    height: 40vw;
    width: 77vw;

    &__oscillator {
        grid-area: ~"1 / 1 / 2 / 5";
    }

    &__filter {
        grid-area: ~"1 / 5 / 2 / 8";
    }

    &__mod-matrix {
        grid-area: ~"1 / 8 / 2 / 10";
    }

    &__controls {
        grid-area: ~"2 / 1 / 3 / 2";
    }

    &__lfo {
        grid-area: ~"2 / 2 / 3 / 4";
    }

    &__envelope {
        grid-area: ~"2 / 4 / 3 / 8";
    }

    &__sequencer {
        grid-area: ~"2 / 8 / 3 / 10";
    }
}
</style>