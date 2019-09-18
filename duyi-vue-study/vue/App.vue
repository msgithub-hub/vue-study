<template>
    <div>
        <h3>线型进度条（百分比外置）</h3>
        <progresses :percentage="0" :showText="false"/>
        <progresses :percentage="30"/>
        <progresses :percentage="50" status="success" />
        <progresses :percentage="70" status="exeption" />
        <br/>
        <br/>
        <h3>线型进度条（百分比内置）</h3>
        <progresses :strokeWith="15" :percentage="50" text-inside="true" />
        <br/>
        <br/>
        <!--<h3>环形进度条</h3>-->
        <!--<progresses  :percentage="50" type="circle" />-->
    </div>
</template>

<script>
    import progresses from "./Progress"
    export default {
        components: {
            progresses,
        },
        data() {
            return {
                name: "黄金福将",
            }
        },


    }
</script>

<style scoped>

</style>