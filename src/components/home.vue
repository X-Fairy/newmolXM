<template>
    <div class="index">
        <!-- 头部菜单 -->
        <Header></Header>
        <!-- 轮播图 -->
        <div class="banner">
            <Carousel v-model="value" loop autoplay  arrow="always" dots="inside"  :autoplay-speed='speed'>
                <CarouselItem>
                    <div class="demo-carousel">
                        <a href="http://www8.53kf.com/m.php?cid=72055204">
                            <img src="@/assets/images/banner/banner6.png" alt="">
                        </a>
                    </div>
                </CarouselItem>
                <CarouselItem>
                    <div class="demo-carousel"><img src="@/assets/images/banner/banner3.png" alt=""></div>
                </CarouselItem>
                <CarouselItem>
                    <div class="demo-carousel"><img src="@/assets/images/banner/banner1.jpg" alt=""></div>
                </CarouselItem>
                <CarouselItem>
                    <div class="demo-carousel"><img src="@/assets/images/banner/banner2.png" alt=""></div>
                </CarouselItem>                
            </Carousel>
        </div>
        <!-- 快速入口 -->
        <div class="entry">
            <div class="entry1">
                <img src="@/assets/images/企业信息.png" alt="" @click="$router.push({path: 'enterprise'})" >
                <a href="tel:4008635888"><img src="@/assets/images/电话资讯.png" alt=""></a>
            </div>
            <div class="entry2">
                <img src="@/assets/images/店面展示.png" alt="" @click="$router.push({path: 'store'})">
                <img src="@/assets/images/招商加盟.png" alt="" @click="$router.push({path: 'orders'})">
            </div>
        </div>
        <div class="main" style="top: 0;margin-bottom: 0;background: #ebebeb;">
            <!-- <img src="@/assets/images/index1.jpg" alt="" @click="$router.push({path: 'enterprise'})" > -->
            <div style="margin: auto;top: 0;text-align:center;width: 100%;">
                <video-player  id="video"  class="video-player vjs-custom-skin"   :options="playerOptions"
                    x-webkit-airplay="allow"
                    x5-video-player-type="h5"
                    x5-playsinline="true"
                    webkit-playsinline="true"
                    :playsinline="playsinline"
                    @canplay="onPlayerCanplay($event)"
                >
                </video-player>
                <!-- <video-player v-if="mobile=='iPhone'" id="video" class="video-player vjs-custom-skin"  :options="playerOptions"></video-player> -->
               <!-- <img src="@/assets/images/play.png" alt="" class="playimg" @click="play"> -->
            </div>
            <!-- <img src="@/assets/images/more.png" alt=""> -->
            <div class="company">
                <div class="f1">
                    <p class="p1">Company Profile</p>
                    <p class="p2">企业介绍</p>
                </div>
                <p class="p">熙美诚品将“物超所值”作为品牌的核心理念，将“持续给消费者创造超越期待的产品”作为企业目标，期待每件拥有自己独特触感的产品，
                都能温柔的融入生活，简单却实用的给消费者传递快乐和惊喜...</p>
                <img src="@/assets/images/more.png" alt="" class="more" @click="$router.push({path: 'enterprise'})">
            </div>
            <div>
                <div class="f1" style="background: #fff;">
                    <p class="p1">Northern Europe Style</p>
                    <p class="p2">北欧风格 简约时尚契合潮流</p>
                </div>
                <Carousel v-model="value1" loop autoplay  arrow="always" class="progress">
                    <CarouselItem>
                        <div class="demo-carousel"><img src="@/assets/images/banner1.jpg" alt=""></div>
                    </CarouselItem>
                    <CarouselItem>
                        <div class="demo-carousel"><img src="@/assets/images/banner2.jpg" alt=""></div>
                    </CarouselItem>
                    <CarouselItem>
                        <div class="demo-carousel"><img src="@/assets/images/banner3.jpg" alt=""></div>
                    </CarouselItem>
                </Carousel>
            </div>
            <div class="market">
                <div class="f1" style="background: #fff;">
                    <p class="p1">Global Overseas Market</p>
                    <p class="p2">熙美诚品海外市场增长迅猛</p>
                </div>
                <h2>熙美诚品全球<span>1600</span>多家门店</h2>
                <h2>覆盖<span>84</span>个国家及地区</h2>
                <img src="@/assets/images/market.jpg" alt="">
                <p style="padding-bottom: 20px; width: 85%;text-indent:2em;">好品牌无国界，截止目前，熙美诚品与<span>美国、加拿大、英国、印度、俄罗斯、新加坡、澳大利亚、巴西沙特阿拉伯等</span>确定了合作伙伴关系 与<span>全球84个国家和地区</span>达成战略合作关系，
                        平均每天有<span>1</span>家熙美诚品开业，特别是东南亚各国、俄罗斯、美国、摩洛哥、迪拜等地区，门店数量正在快速递增，熙美诚品，全球从业人员<span>8000</span>多，熙美诚品通过<span>6000</span>多款物超所值的产品，每天向全球消费者传递快乐和惊喜！
                </p>
            </div>
            <div class="goodness">
                <div class="f1">
                    <p class="p1">Global Overseas Market</p>
                    <p class="p2" style="color: #fff;">10大核心竞争力</p>
                </div>
                <ul>
                    <li>
                        <p style="font-size: 14px;">军事化管理团队</p>
                        <p>作风过硬，保障有力，超强执行力团队</p>
                    </li>
                    <li>
                        <p style="font-size: 14px;">50000平方米仓储物流中心</p>
                        <p>为客户提供无忧的货品供给，3.9亿库存</p>
                    </li>
                    <li>
                        <p style="font-size: 14px;">二店率高达38%</p>
                        <p>老加盟商开2店或多店超过400家</p>
                    </li>
                    <li>
                        <p style="font-size: 14px;">10年行业沉淀</p>
                        <p>大数据基础、团队基础、供应链基础</p>
                    </li>
                    <li>
                        <p style="font-size: 14px;">1000家优质产品供应商</p>
                        <p>50%合作5年以上的优质供应商，产品质量是企业的生命线</p>
                    </li>
                    <li>
                        <p style="font-size: 14px;">天下武功，唯快不破</p>
                        <p>平均每个月800款新品的速度、同行业的标杆</p>
                    </li>
                    <li>
                        <p style="font-size: 14px;">6个大区，3个分公司</p>
                        <p>督导下店，服务范围覆盖全国，平均每季度下店服务超过900家店</p>
                    </li>
                    <li>
                        <p style="font-size: 14px;">供应链</p>
                        <p> 6000款SKU，百分百全系列定制产品，品质有保证，首批货品百分百调换货政策</p>
                    </li>
                    <li>
                        <p style="font-size: 14px;">全年度12场商学院培训会</p>
                        <p>行业人才孵化器，六个大区巡回培训</p>
                    </li>
                    <li>
                        <p style="font-size: 14px;">整店输出 </p>
                        <p>选址、开业、货品供给、督导下店，全程持续服务，让加盟商开店无忧</p>
                    </li>
                </ul>
                <img src="@/assets/images/goodness.jpg" alt="" style="width: 91%;display: block;margin: auto;padding-bottom: 20px;">
            </div>
            <div class="category">
                <div class="f1" style="background: #fff;">
                    <p class="p1">Product Categories</p>
                    <p class="p2">产品分类</p>
                </div>
                <img src="@/assets/images/category.jpg" alt="" style="width: 91%;display: block;margin: auto;" @click="$router.push({path: 'product'})">
                <div class="benefit">
                    <img src="@/assets/images/benefit.jpg" alt="">
                    <h2>全面的开启支持体系</h2>
                    <ul>
                        <p>解决经营痛点，让你开店无忧</p>
                        <li>免费提供店面地址，专业评估店面可行性</li>
                        <li>免费设计店铺，提供装修指导</li>
                        <li>海鼎ESHOP收银软件，了解爆款热销产品清单</li>
                        <li>高级督导老师下店指导，提升店面营业额</li>
                        <li>每月商学院培训支持，提高店铺运营管理能力</li>
                    </ul>
                    
                </div>
                
            </div>
            <div class="store">
                <div class="f1" style="background: #fff;">
                    <p class="p1">Public Praise & Popularity</p>
                    <p class="p2">口碑好店 人气爆棚</p>
                </div>
                <ul class="storeImg" >
                        <!-- @click="large" -->
                    <li>
                        <img src="@/assets/images/index/store_03.png" alt="" style="width: 49%;height: 90px;">
                        <img src="@/assets/images/index/store_05.png" alt="" style="width: 25%;height: 90px;">
                        <img src="@/assets/images/index/store_07.png" alt="" style="width: 25%;height: 90px;">
                    </li>
                    <li >
                        <img src="@/assets/images/index/store_13.png" alt="" style="width: 30%;height: 165px;">
                        <div class="one">
                            <div class="two">
                                <img src="@/assets/images/index/store_15.png" alt="" style="width: 60%;height: 80px;">
                                <img src="@/assets/images/index/store_16.png" alt="" style="width: 39%;height: 80px;">
                            </div>
                            <div class="two" style="margin-bottom: 0;">
                                <img src="@/assets/images/index/store_19.png" alt="" style="width: 39%;height: 80px;">
                                <img src="@/assets/images/index/store_21.png" alt="" style="width: 60%;height: 80px;">
                            </div>        
                        </div>
                    </li>
                    <li>
                        <div style="width: 50%;height: 100%;display: flex;justify-content: space-between;flex-wrap: wrap;">
                            <img src="@/assets/images/index/store_25.png" alt="" style="width:50%;height: 50%;">
                            <img src="@/assets/images/index/store_26.png" alt="" style="width: 49%;height: 50%;">
                            <img src="@/assets/images/index/store_33.png" alt="" style="width: 100%;height: 48%;">
                        </div>
                        
                            <img src="@/assets/images/index/store_27.png" alt="" style="width: 24%;height: 100%">
                       
                        <div style="width: 24%;height:100%">
                            <img src="@/assets/images/index/store_29.png" alt="" style="width: 100%;height: 50%;">
                            <img src="@/assets/images/index/store_36.jpg" alt="" style="width: 100%;height: 50%;">
                        </div>
                        
                    </li>
                </ul>
                <!-- <img src="@/assets/images/index2.jpg" alt=""> -->
            </div>
            
            <div class="news">
                <div class="info">
                    <img src="@/assets/images/newBanner.jpg" alt="">
                    <div class="content" v-for="(item,index) in newList" :key="index" @click="detail(item.id)">
                        <p class="title">{{item.title}}</p>
                        <p class="time">{{item.editeddate}}</p>
                    </div>
                    <img src="@/assets/images/more.png" alt="" class="more" @click="$router.push({path: 'news'})">
                </div>
            </div>
        </div>
        <Modal v-model="Modal" title="查看大图" >
            <img :src="src" alt="">
        </Modal>
        <BackTop :bottom="50" :right="10">
            <div class="top"><span class="iconfont">&#xe63f;</span></div>
        </BackTop>
        <!-- 底部内容 -->
        <!-- <Bottom></Bottom> -->
        <!-- <Alert></Alert> -->
        <Footer v-show="show"></Footer>
        <!-- <Msg></Msg> -->
    </div>
</template>
<script>
import Header from '@/components/header.vue'
import Footer from '@/components/footer.vue'
import Msg from '@/components/msg.vue'
import https from '@/http.js'
import Bottom from '@/components/bottom.vue'
export default {
    data(){
        return{
            
            playerOptions :	{
                // playbackRates: [0.7, 1.0, 1.5, 2.0], //播放速度
                preload: 'auto', // 建议浏览器在<video>加载元素后是否应该开始下载视频数据。auto浏览器选择最佳行为,立即开始加载视频（如果浏览器支持）
                language: 'zh-CN',
                aspectRatio: '16:9', // 将播放器置于流畅模式，并在计算播放器的动态大小时使用该值。值应该代表一个比例 - 用冒号分隔的两个数字（例如"16:9"或"4:3"）
                fluid: true, // 当true时，Video.js player将拥有流体大小。换句话说，它将按比例缩放以适应其容器。
                sources: [{
                    type: 'video/mp4',
                    src: "../../static/熙美十周年盛典.mp4", //url地址
                }],
                poster: "../../static/img/video.jpg", //你的封面地址
                notSupportedMessage: '此视频暂无法播放，请稍后再试', //允许覆盖Video.js无法播放媒体源时显示的默认信息。
                // controlBar: {
                //     timeDivider: true,
                //     durationDisplay: true,
                //     remainingTimeDisplay: false,
                //     fullscreenToggle: true  //全屏按钮
                // }
                
            },
            value:0,
            value1:0,
            show:false,
            newList:[],
            Modal:false,
            src:'',
            mobile:"",
            text:"",
            speed:5000

        }
    },
    components: {
        Header,
        Footer,
        Msg,
        
    },
    created () {
        this.getnew();
        const that = this
        that.timer = setInterval(function () {
            if (document.readyState === 'complete') {
               that.show=true;
                window.clearInterval(that.timer)
            }
        }, 1000);
        
    },
    computed: {
        playsinline(){
    		var ua = navigator.userAgent.toLocaleLowerCase(); //x5内核
            if (ua.match(/tencenttraveler/) != null || ua.match(/qqbrowse/) != null) {
                return false
            }else{
                //ios端
                return true				
            }
            }
    },
    methods:{       
        getnew(){
            https.get('/gyanwang/index.php/Home/Index/homepage').then((data) => {
               this.newList=data.data;
               this.newList.forEach(ele=>{
                   ele.editeddate.substr(10,9);
               })
            }).catch((err)=>{
                console.log(err)

            })
        },
        play(){
            var video =$('#video');
            
            if(video.paused){
              video.play();
            }else if(video.play()){
               video.pause();
             }
        },
       large(e){
           this.src=e.target.src;
           this.Modal=true;
       },
       //在vue-video-player的onPlayerCanplay(视频可播放)这个方法中添加回调
        onPlayerCanplay(player) {
            // console.log('player Canplay!', player)
            //解决自动全屏
            var ua = navigator.userAgent.toLocaleLowerCase();
            //x5内核
            if (ua.match(/tencenttraveler/) != null || ua.match(/qqbrowse/) != null) {
                $('body').find('video').attr('x-webkit-airplay',true).attr('x5-playsinline',true).attr('webkit-playsinline',true).attr('playsinline',true)
            }else{
                //ios端
                $('body').find('video').attr('webkit-playsinline',"true").attr('playsinline',"true") 
                
            }

        },
        // 查看文章详情
        detail(id){
            this.$router.push({path:'/newDetail',query:{num:id}})
        }
    }
}
</script>

    
    
    
    