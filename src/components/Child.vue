<template>
    <h3>Child</h3>
    <button @click="clickEventHandle">子元素按钮</button>
</template>
<script>
/**
 * 父传子 ： props
 * 子传父 ： 自定义事件(this.$emit)
 */
export default {

    data() {
        return {
            message: "子元素传递的数据"
        }
    },
    methods: {
        clickEventHandle() {
            this.$emit("someEvent", this.message)
        }
    }
}
</script>