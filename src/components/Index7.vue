<template>
    <div>
        <!-- <vue-marquee></vue-marquee> -->
        <div class="iftop05">
        <iframe ref="iframe" id="bdIframe" :src="bdTokenUrl" frameborder="0" scrolling="no" width="100%" height="2500px" ></iframe>
        </div>
    </div>
</template>

<script>
    import marquee from './../components/marquee01';
    export default {
        data() {
            return {
                bdTokenUrl: 'http://tiyu.baidu.com/home' //https://m.sporttery.cn/app/zf/fb/livelist.html  https://m.sporttery.cn/app/zf/fb/livelist.html http://m.sporttery.cn/wap/dtc/fb_league_europe.html
            }
        },
        // created() {
        //     this.getUrl();
        //     this.$nextTick(()=>{
        //         this.getCode();
        //     });
        // },
        mounted(){
            /**
             * iframe-宽高自适应显示   
            */
            const oIframe = document.getElementById('bdIframe');
            const deviceWidth = document.documentElement.clientWidth;
            const deviceHeight = document.documentElement.clientHeight;
            oIframe.style.width =  '100%'; //数字是页面布局宽度差值
            oIframe.style.height = '2500px'; //数字是页面布局高度差
        },
        components: {
         'vue-marquee':marquee
        },
    }
</script>

<style lang="scss" scoped>
@import "scss/base.scss";
.child-view{
    height:100%;
}
.iftop05{
    height: 100%;
    margin-top:-83px;
    margin-bottom:60px;
}
</style>