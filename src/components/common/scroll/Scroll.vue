<template>
    <div class="wrapper" ref="wrapper">
        <div class="content">
            <slot></slot>
        </div>
    </div>
</template>

<script>
import BScroll, { PullUpLoad } from "better-scroll";

export default {
    name: 'Scroll',
    props: {
        probeType: {
            type: Number,
            defualt: 0
        },
        pullUpLoad: {
            type: Boolean,
            defualt: false
        }
    },
    data() {
        return {
            scroll: null,
        }
    },
    mounted() {
        this.scroll = new BScroll(this.$refs.wrapper, {
            click: true,
            // taps: true
            probeType: this.probeType,
            pullUpLoad: this.pullUpLoad,
            // pullUpLoad: true,
        })

        this.scroll.on('scroll', (position) => {
            // console.log(position)
            this.$emit('scroll', position)
        })

        this.scroll.on('pullingUp', () => {
            // console.log('load more')
            this.$emit('pullingUp')
        })
    }
}
</script>

<style scoped>

</style>