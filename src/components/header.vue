<template>
    <div class="header">
        <div class="header-content">
            <div class="left">
                <img src="@/assets/images/logo.jpg" alt=""  @click="index">
            </div>
            <div class="right">
                <a href="tel:4008635888" style="width: 70%;"><img src="@/assets/images/400.jpg" alt=""></a>
                <div class="icon" @click="nav">
                    <svg v-if="navShow==false" style="margin: auto;width: 25px;height: 25px;" t="1572256972129" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="7767" width="10" height="10"><path d="M0 452.736m32 0l960 0q32 0 32 32l0 0q0 32-32 32l-960 0q-32 0-32-32l0 0q0-32 32-32Z" p-id="7768" fill="#1d8c9f"></path><path d="M0 140.16m32 0l960 0q32 0 32 32l0 0q0 32-32 32l-960 0q-32 0-32-32l0 0q0-32 32-32Z" p-id="7769" fill="#1d8c9f"></path><path d="M0 809.856m32 0l960 0q32 0 32 32l0 0q0 32-32 32l-960 0q-32 0-32-32l0 0q0-32 32-32Z" p-id="7770"  fill="#1d8c9f"></path></svg>
                    <svg @cilck="navShow=false" v-else style="margin: auto;width: 25px;height: 25px;" t="1572256578841" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="5206" width="10" height="10"><path d="M574.55 522.35L904.4 192.5c16.65-16.65 16.65-44.1 0-60.75l-1.8-1.8c-16.65-16.65-44.1-16.65-60.75 0L512 460.25l-329.85-330.3c-16.65-16.65-44.1-16.65-60.75 0l-1.8 1.8c-17.1 16.65-17.1 44.1 0 60.75l329.85 329.85L119.6 852.2c-16.65 16.65-16.65 44.1 0 60.75l1.8 1.8c16.65 16.65 44.1 16.65 60.75 0L512 584.9l329.85 329.85c16.65 16.65 44.1 16.65 60.75 0l1.8-1.8c16.65-16.65 16.65-44.1 0-60.75L574.55 522.35z" p-id="5207" fill="#1d8c9f"></path></svg>
                    <!-- <svg @cilck="navShow=false" v-else style="margin: auto;width: 25px;height: 25px;" t="1572256478164" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="3387" width="10" height="100"><path d="M34.32448 14.09024h955.35104v199.168H34.32448zM34.32448 412.42624h955.35104v199.168H34.32448zM34.32448 810.76224h955.35104v199.168H34.32448z" p-id="3388" fill="#1d8c9f"></path></svg> -->
                    <!-- <svg style="margin: auto;width: 25px;height: 25px;" t="1569824399835" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="962" width="10" height="10"><path d="M790.890174 453.094706c-219.398589 0.07875-219.398589 0.07875-219.556089-217.114828C571.097834 0.201208 571.097834 0.201208 803.962739 0.201208c219.71359 0.07875 219.71359 0.07875 220.028592 217.036077 0.393752 235.85742 0.393752 235.85742-233.101157 235.857421zM807.349006 72.494067C647.800714 72.494067 643.390693 75.959084 643.233192 200.935954c-0.236251 179.865892-0.236251 179.865892 167.817082 180.023394 137.02568 0.157501 140.569448-3.701268 140.648198-152.145755C951.777223 73.202821 951.22597 72.572817 807.349006 72.494067z m-11.340056 498.411223c227.982381 0 227.982381 0 227.903631 225.226118-0.07875 227.352378-0.07875 227.352378-225.304868 227.588629-227.037377 0.236251-227.037377 0.236251-227.431129-224.989866-0.393752-227.82488-0.393752-227.82488 224.832366-227.824881z m-35.673927 380.679389c190.497195 0.787504 190.969698 0.472502 191.363449-124.819369 0.472502-180.023393-1.653758-183.094659-124.898119-183.40966-182.937158-0.472502-182.937158-0.472502-183.33091 148.680737-0.472502 151.20075 5.276276 159.075789 116.86558 159.548292z m-531.643888-498.489973C0.472502 452.543453 0.472502 452.543453 0.472502 221.096054 0.393752 0.358709 0.393752 0.358709 224.202362 0.279959c228.848636 0 228.848636 0 229.006137 232.077401 0.157501 221.209848 0.157501 221.209848-224.517364 220.737346zM244.126211 72.572817C75.049122 72.179066 72.686611 73.990325 72.52911 201.250956 72.214108 379.620591 73.001612 380.644346 201.128498 380.801847c179.39339 0.236251 179.39339 0.236251 179.629641-152.303256C380.91564 77.14034 377.135621 72.887819 244.126211 72.572817z m-25.830128 498.568724c234.912416-0.07875 234.912416-0.07875 234.754915 234.046162-0.07875 218.138582-0.07875 218.138582-218.532334 218.768585-234.439913 0.551253-234.439913 0.551253-234.203662-234.203662 0.236251-218.532334 0.236251-218.532334 217.981081-218.611085z m4.252521 380.443138c149.546992 0.472502 157.973284-5.827529 158.288286-118.283087 0.630003-185.45717-2.04751-189.709691-118.204337-190.024693C77.411634 642.725647 72.922862 645.48191 72.450359 761.559986c-0.787504 189.552191-0.787504 189.552191 150.098245 190.024693z" fill="#1d8c9f" p-id="963"></path></svg> -->
                </div>
                
            </div>
        </div>
        <div class="nav" v-show="navShow">
            <ul @click="top">
                <li @click="$router.push({path: '/'})">首页</li>
                <li @click="$router.push({path: 'enterprise'})">企业介绍</li>
                <li @click="$router.push({path: 'orders'})">招商加盟</li>
                <li @click="$router.push({path: 'store'})">店面展示</li>
                <li @click="$router.push({path: 'news'})">资讯新闻</li>
                <!-- <li @click="$router.push({path: 'publicGood'})">熙美公益</li> -->
                <li @click="$router.push({path: 'school'})">商学院</li>
                <li @click="$router.push({path: 'product'})">产品分类</li>
            </ul>
            <div style="height: 60px;width: 100%;">
                <a href="tel:4008635888"><img src="@/assets/images/phone.png" alt=""></a>
            </div>
        </div>
        <Bottom></Bottom>
        <!-- <Alert></Alert> -->
    </div>
</template>

<script>
import { Swipe, SwipeItem } from 'mint-ui';
import Bottom from '@/components/bottom.vue'
import Alert  from '@/components/alert.vue'
export default {
    data(){
        return {
            // 是否出现导航菜单
            navShow:false,
        }
    },
    components: {
        Swipe,
        SwipeItem,
        Bottom,
        Alert
    },
    methods:{
        nav(){
            if(this.navShow===true){
                this.navShow=false;
            }else{
                this.navShow=true;
            }
        },
        top(){
            document.scrollingElement.scrollTop=0;
        },
        index(){
            this.$router.push({path: '/'});
            document.scrollingElement.scrollTop=0;

        }
    }
}
</script>




