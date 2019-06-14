<template>
    <div class="demo-image">

        <div>
        <span>预测得太准啦！给开发者们买杯咖啡吧：）</span>
        </div>
        <div class="image-center">
        <el-tabs v-model="activeName" @tab-click="handleClick">
            <el-tab-pane label="支付宝" name="first">
                <img src="../common/img/alipay.jpg"/>
            </el-tab-pane>
            <el-tab-pane label="微信" name="second">
                <img src="../common/img/wechatpay.jpg"/>
            </el-tab-pane>

        </el-tabs>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                activeName: 'second'

            }
        },
        methods: {
            handleClick(tab, event) {
                console.log(tab, event);
            }
        }
    }
</script>

<style lang="scss" scoped>
    .demo-image{
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        width:100%;
        height:100%;
        .image-center{
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            width:100%;
            height:100%;
        }
    }
    img{
        margin-left:50%;
        transform: translateX(-50%);
        width:50%;
        height:50%;
    }


</style>
