<template>
    <view class="hello-wrap">
        <button plain class="hello-btn" @click="handleClick">Hello in {{from}}</button>
    </view>
</template>
<script>
export default {
    config: {
    },

    props: {
        from: String
    },

    components: {
    },

    data: {
    },

    methods: {
        handleClick() {
            this.$emit('hello', {from: this.from});
        }
    }
};
</script>
<style lang="stylus">
.hello-wrap
    padding: 20px
    margin: 20px 0

    .hello-btn
        width: 500px
        height: 148px
        margin: 0 auto
        -quick-margin: 0
        -quick-justify-content: center
        -quick-align-items: center
        line-height: @height
        background-color: #fff
        text-align: center
        border-radius: 120px
        border: 0
        &:after
            -tt-border: none
</style>
