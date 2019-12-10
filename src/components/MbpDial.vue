<template>
    <div class="mbp-dial">
        <img class="mbp-dial__button"
            src="../assets/dial.svg"
            :style="style"
            @mousedown.prevent="addListener" />
    </div>
</template>

<script>
export default {
    computed: {
        style() {
            const rotate = this.value - 135;
            return {
                transform: `rotate(${rotate}deg)`
            };
        }
    },

    data() {
        return {
            initialValue: null,
            initialX: null,
            value: 0,
        }
    },

    methods: {
        addListener(e) {
            this.removeListener();
            this.initialValue = this.value;
            this.initialX = e.clientX;
            window && window.addEventListener("mousemove", this.onMouseMove);
        }, 
        
        removeListener() {
            window && window.removeEventListener("mousemove", this.onMouseMove);
        },

        onMouseMove(e) {
            e.preventDefault();
            let v = this.initialValue + e.clientX - this.initialX;
            if (v > 270) v = 270;
            if (v < 0) v = 0;

            this.value = v;

            if (e.buttons !== 1)
                this.removeListener();
        },
    },
}
</script>

<style lang="less">
.mbp-dial {
    background: url("../assets/dial-markings.svg") no-repeat;
    box-sizing: border-box;
    display: inline-flex;
    padding: .17em;
    font-size: 150px;

    &__button {
        height: 1em;
        width: 1em;
    }
}
</style>