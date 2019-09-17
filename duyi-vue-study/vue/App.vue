<template>
    <!--<div>我爱你！{{ name }}</div>-->
    <Progress :percentage="30"/>
</template>

<script>
    import Progress from "./Progress"

    export default {
        data() {
            return {
                name: "黄金福将",
            }
        },
        components: {
            Progress
        }

    }
</script>

<style scoped>

</style>