<template>
    <div class="store">
         <!-- 头部菜单 -->
        <Header></Header>
        <div class="main">
            <img src="@/assets/images/school/shadow.jpg" alt="">
            <div class="store1">
                <div class="f1" style="background:#fff;padding-top: 0;">
                    <p class="p1">Store Image Upgrade</p>
                    <p class="p2">全新店面升级</p>
                </div>
                <img src="@/assets/images/store/1.jpg" alt="">
                <p class="item-content">熙美诚品全新店铺形象，以北欧风为基调，空间色彩采用马尔斯绿，视觉统一；在产品的陈列上，从颜色、质感、款式等方面匹配货柜设计，高低组合、错落有致，让每款产品出现在最合适的位置上，从细节上体现品牌对完美和高品质的追求，给顾客带来舒适的视觉感受和购物体验。</p>
                <div class="img-item">
                    <img src="@/assets/images/store/2.jpg" alt="">
                    <img src="@/assets/images/store/3.jpg" alt="">
                </div>
                <p class="item-content">在产品的陈列上，全新的货柜设计，高低组合错位，从颜色、质感、款式上让每件产品出现在最合适的位置上，
                    细节上体现品牌对完美和高品质的追求，给顾客带来视觉上的冲击以及最舒适的产品体验。</p>
                <img src="@/assets/images/store/4.jpg" alt="" style="width: 90%;margin: auto;display: block;">
            </div>
            <div class="store2">
                <div class="f1" style="background:#fff;">
                    <p class="p1">Store Display</p>
                    <p class="p2">店面展示</p>
                </div>
                <ul class="img-item" >
                        <!-- @click="large" -->
                    <li class="two">
                        <div>
                            <img src="@/assets/images/store/images/店铺_03.jpg" alt="">
                            <img src="@/assets/images/store/images/店铺_07.jpg" alt="">
                        </div>
                        <img src="@/assets/images/store/images/店铺_05.jpg" alt="">
                        
                    </li>
                    <li class="one">
                        <img src="@/assets/images/store/images/店铺_10.jpg" alt="">
                    </li>
                    <li class="three">
                        <img src="@/assets/images/store/images/店铺_12.jpg" alt="">
                        <img src="@/assets/images/store/images/店铺_14.jpg" alt="">
                        <img src="@/assets/images/store/images/店铺_16.jpg" alt="">
                    </li>
                    <li class="three">
                        <img src="@/assets/images/store/images/店铺_20.jpg" alt="">
                        <img src="@/assets/images/store/images/店铺_22.jpg" alt="">
                        <img src="@/assets/images/store/images/店铺_23.jpg" alt="">
                    </li>
                    <li class="one"><img src="@/assets/images/store/images/店铺_27.jpg" alt=""></li>
                    <li class="one"><img src="@/assets/images/store/images/店铺_29.jpg" alt=""></li>
                </ul>
            </div>
             <!-- <img src="@/assets/images/店铺.jpg" alt=""> -->
        </div>
        <Modal v-model="Modal" title="查看大图" >
            <img :src="src" alt="">
        </Modal>
        <BackTop :bottom="50" :right="10">
            <div class="top"><span class="iconfont">&#xe63f;</span></div>
        </BackTop>
        <!-- 底部内容 -->
        <Footer v-show="show"></Footer>
        <!-- <Msg></Msg> -->
    </div>
</template>
<script>
import Header from '@/components/header.vue'
import Footer from '@/components/footer.vue'
import Msg from '@/components/msg.vue'
export default {
    data(){
        return {
            show:false,
            // 大图地址
            src:'',
            Modal:false
        }
    },
    components: {
        Header,
        Footer,
        Msg
    },
    created () {
        const that = this
        that.timer = setInterval(function () {
            if (document.readyState === 'complete') {
               that.show=true;
                window.clearInterval(that.timer)
            }
        }, 1000)
    },
    methods:{
        large(e){
            console.log(e.target.src);
            this.src=e.target.src;
            this.Modal=true;
        }
    }
}
</script>