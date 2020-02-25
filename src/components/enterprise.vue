<template>
    <div class="enterprise">
        <!-- 头部菜单 -->
        <Header></Header>
        
        <div class="main">
                
            <div class="floor1">
                <div class="part1">
                    <img src="@/assets/images/company/index1.png" alt="">
                </div>
                <div class="part2">
                    <div class="info">
                        <h4>CORPORATE CULYURE</h4>
                        <h1>熙美企业文化</h1>
                    </div>
                    <img src="@/assets/images/company/index2.png" alt="" style="margin-top: -10px;width:100%;">
                    <ul class="infos">
                        <li>
                            <p class="one">我们的使命</p>
                            <P class="line"></P>
                            <p class="two">向全球消费者传递快乐和惊喜</p>
                            <p class="three">We Deliver Happiness and Surprises To the Global Consumers</p>
                        </li>
                        <li>
                            <p class="one">我们的愿景</p>
                            <P class="line"></P>
                            <p class="two">做快时尚百货第一品牌</p>
                            <p class="three">To Be the First Brand of Fast fashion General Merchandise</p>
                        </li>
                        <li >
                            <p class="one">核心价值观</p>
                            <P class="line"></P>
                            <p class="two">诚信、团结、创新、高效、责任、感恩、利他</p>
                            <p class="three">Integrity, Unity, Innovation, Efficiency, Responsibility, Gratidute and Altruism</p>
                        </li>
                    </ul>
                </div>
                
            </div>
            <Carousel v-model="value1" loop autoplay  arrow="never" class="progress address">
                <CarouselItem>
                    <div class="demo-carousel">
                        <img src="@/assets/images/company/banner1.jpg" alt="">
                        <div>
                            <p class="china">华东总部——杭州</p>
                            <p class="eng">HANGZHOU</p>
                        </div>
                    </div>
                </CarouselItem>
                <CarouselItem>
                    <div class="demo-carousel">
                        <img src="@/assets/images/company/banner2.jpg" alt="">
                        <div>
                            <p class="china">仓储物流中心——义乌</p>
                            <p class="eng">YIWU</p>
                        </div>
                    </div>
                </CarouselItem>
                <CarouselItem>
                    <div class="demo-carousel">
                        <img src="@/assets/images/company/banner3.jpg" alt="">
                        <div>
                            <p class="china">华南总部——广州</p>
                            <p class="eng">GUANGZHOU</p>
                        </div>
                    </div>
                </CarouselItem>
            </Carousel>
            <div class="floor0">
                <!-- <img src="@/assets/images/company/earth.jpg" alt=""> -->
                <p class="floor-content" style="padding-bottom:0;">XIMIVOGUE熙美诚品，是集品质、价格、创意、设计、供应和销售于一体，为全球消费者传递快乐和惊喜的快时尚百货品牌。以“物超所值”为核心理念，超强整合生活百货、彩妆护肤、文体礼品、饰品系列、休闲食品、精美包饰、毛绒玩具、数码配件、季节产品等九大品类，竭尽全力为全球消费者打造超越他们预期的产品。</p>
                <p class="floor-content" style="padding:0px 20px;">截止2019年10月，熙美诚品拥有超过5万平方的综合性产业园，1000多家优质供应商，8大运营中心，7大区督导服务，从业人员达8000多人。</p>
                <p class="floor-content" style="padding-top:0">目前，熙美诚品全球加盟店已经突破1600家，店铺遍布全球84个国家及地区，熙美诚品通过持续开发物超所值的产品，向全球消费者传递快乐和惊喜！</p>
                
            </div>
            <div class="floor2">
                <div class="f1" style="background: none;">
                    <p class="p1">Cooperative Brand</p>
                    <p class="p2">品牌合作伙伴</p>
                </div>
                <p style="padding: 0 25px;line-height: 25px;letter-spacing: 1px;text-indent: 2em;">熙美诚品与小猪佩奇、哆啦A梦、大头儿子小头爸爸、熊出没、海底小纵队、迪士尼、精灵宝可梦、kakao friends、B.DUCK、奥特曼、漫威、芝麻街、小黄人等知名品牌建立正版授权合作关系，拥有1000家优质供应商，50%以上都是合作5年以上，产品货源稳定有保障，每月800款SKU更新的速度，能迅速抓住消费者注意力，保证复购率，提高门店营业额。
                </p>
                <img src="@/assets/images/company/Partners.jpg" alt="" style="width: 90%;display: block;margin: auto;">
            </div>
            <div class="market">
                <div class="f1" style="background: #fff;">
                    <p class="p1">Global Overseas Market</p>
                    <p class="p2">熙美诚品海外市场增长迅猛</p>
                </div>
                <p style="padding-bottom: 20px; width: 85%;text-indent: 2em;">好品牌无国界，截至目前，熙美诚品与<span>美国、英国、印度、加拿大、俄罗斯、新加坡、澳大利亚、巴西沙特阿拉伯</span>等确定了合作伙伴关系
                    ，与<span>全球84个国家和地区</span>达成战略合作协议，平均每天有1家熙美诚品开业，特别是在<span>东南亚各国、俄罗斯、美国、摩洛哥、迪拜</span>等地区，
                    门店数量正在快速递增。
                </p>
                <img src="@/assets/images/market.jpg" alt="">
                <p style="padding-bottom: 20px; width: 85%;text-indent: 2em;">熙美诚品，全球从业人员8000多，熙美诚品通过6000多款物超所值的产品，每天向全球消费者传递快乐和惊喜！</p>
            </div>
            <div class="floor3">
                <div class="f1" style="background: none;">
                    <p class="p1">Corporate Culture</p>
                    <p class="p2">企业文化</p>
                </div>
                <ul>
                    <li>
                        <h2>军队/ARMY</h2>
                        <p>定义：是！保证完成任务，不找借口，只找方法，坚决执行</p>
                        <span>内涵：使命、纪律、忠诚、责任、荣誉</span>
                    </li>
                    <li>
                        <h2>学校/SCHOOL</h2>
                        <p>定义：快乐每一天，学习榜样，调整心态，比学赶帮超</p>
                        <span>内涵：学习、互助、成长、分享、友谊</span>
                    </li>
                    <li>
                        <h2>家庭/FAMILY</h2>
                        <p>定义：我们都是一家人，你的事就是我的事，友爱互助，心存感恩</p>
                        <span>内涵：责任、奉献、亲情、微笑、担当</span>
                    </li>
                </ul>
            </div>
            <div class="floor4">
                <img src="@/assets/images/company/index3.png" alt="">
                <div class="progress">
                    <img src="@/assets/images/company/index4.png" alt="">
                    <h4>十年发展历程</h4>
                    <div class="content">
                        <ul class="one">                           
                            <li>  
                                <p class="time">2010年</p>
                                <p>单店数量达到 9家 开启直营管理模式。</p>
                                <img src="@/assets/images/company/2010.png" alt="">                            
                            </li>
                            <li>
                                <p class="time">2014年</p>
                                <p>加盟门店超过 1000家。</p>
                                <img src="@/assets/images/company/2014.png" alt="">
                            </li>                            
                            <li>
                                <p class="time">2016年</p>
                                <p>熙美诚品董事长受邀参加CCTV、《对话中国品牌》栏目访谈，仓储物流升级，迁至新的仓储基地，成立熙美诚品商学院，全年度12场商学院培训。
                                </p>
                                <img src="@/assets/images/company/2016.png" alt="">
                            </li>
                            <li>
                                <p class="time">2018年</p>
                                <p>杭州华城国际发展大厦成立华东总部，熙美诚品遍布全球77个国家及地区。</p>
                                <img src="@/assets/images/company/2018.png" alt="">
                            </li>
                        </ul>
                        <ul class="two">
                            <li>
                                <p class="time">2009年</p>
                                <p>第一家直营店在南京开业。</p>
                                <img src="@/assets/images/company/2009.png" alt="">
                            </li>
                            <li>
                                <p class="time">2012年</p>
                                <p> 设立总部于中国·义乌，正式开放加盟渠道。</p>
                                <img src="@/assets/images/company/2012.png" alt="">
                            </li>
                            <li > 
                                <p class="time">2015年</p>
                                <p>饰品加盟转型，成立快时尚百货--熙美诚品,同年全国门店加盟超过300家,熙美诚品正式加入中国青少年发展基金会。</p> 
                                <img src="@/assets/images/company/2015.png" alt="">                    
                            </li>
                            <li>
                                <p class="time">2017年</p>
                                <p> 广州国际金融中心成立华南总部，国际事业部成立
                                        门店数量突破1000家
                                    “熙美诚品专项公益基金”正式成立。
                                </p>
                                <img src="@/assets/images/company/2017.png" alt="">
                            </li>
                            <li>
                                <p class="time">2019年</p>
                                <p>熙美诚品成立10周年，捐建第10所希望小学，熙美诚品加盟店突破1600家，遍布全国84个国家及地区。</p>
                                <img src="@/assets/images/company/2019.png" alt="">
                            </li>
                        </ul>
                    </div>
                </div>
                
            </div>
        </div>
        <BackTop :bottom="50" :right="10">
                <div class="top"><span class="iconfont">&#xe63f;</span></div>
        </BackTop>
        <!-- 底部内容 -->
        <Footer v-show="show"></Footer>
        <!-- <msg></msg> -->
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
            value1:0
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
        
    }
}
</script>