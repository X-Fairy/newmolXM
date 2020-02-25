<template>
    <div class="footer">
       <div class="concat">
           <!-- @click="modal1=true" -->
           <img src="@/assets/images/concat.jpg" alt="">
       </div>
       <div class="bottom">
           <div>
                <h3>义乌总部</h3>
                <p>浙江省义乌市丹溪北路728号</p>
                <h3>华东分部</h3>
                <p>浙江杭州华成国际发展大厦19F</p>
                <h3>华南分部</h3>
                <p>广州国际金融中心1802-1803单元</p>
                <!-- 4000 -->
                <!-- <h3>南京分公司</h3>
                <p>江苏省南京市太平南路1号新世纪广场B座2116</p>
                <h3>成都分公司</h3>
                <p>四川省成都市锦江区盐市口东御街19号茂业天地3807室</p>
                <h3>北京分公司</h3>
                <p>北京市通州区蓝调沙龙小区4号楼302室</p> -->
           </div>
           <div>
               <h3>供应商合作</h3>
               <p>电话：0579-85893900</p>
               <p>邮箱：22245727@qq.com</p>
           </div>
           <div>
               <img src="@/assets/images/LOGO.png" alt="">
               <h3>免费热线：400-863-5888</h3>
               <p>@2019熙美诚品 版权所有 ALL Rights Reserved</p>
               <p>网站所属：{{content}}</p>
               <P>ICP号：{{icp}}</P>
           </div>
           <div style="font-size:12px;">
               <p>市场有风险，投资需谨慎</p>
               <p>数据来源于熙美诚品品牌运营中心</p>
           </div>
       </div>
    </div>
</template>
<script>
export default {
    data(){
        return {
            // 是否显示弹出框
            // modal1:false,
            // 填写表单
            formValidate:{
                name: '',
                phone:'',
            },
            ruleValidate: {
                name: [
                    { required: true, message: '姓名不能为空', trigger: 'blur' }
                ],
                phone: [
                    {  type: 'number',required: true, message: '电话不能为空', trigger: 'blur' },
                ],
            },
            content:'广州熙彬贸易有限公司',
            icp:'粤ICP备17127451号-1'
        }
    },
    created(){
       this.change()
    },
    methods:{        
        handleSubmit (name) {
            this.$refs[name].validate((valid) => {
                if (valid) {
                    this.$Message.success('Success!');
                } else {
                    this.$Message.error('Fail!');
                }
            })
        },
        change(){
            if(location.href.includes('xmvogue')){
                this.content='广州熙彬贸易有限公司';
                this.icp='粤ICP备17127451号-1';
            }else if(location.href.includes('xmcpcn')){
                this.content='义乌楚睿电子商务有限公司';
                this.icp='浙ICP备13017989号-2'
            }else if(location.href.includes('4008635888')){
                this.content='浙江熙彬进出口有限公司';
                this.icp='浙ICP备18051049号-1'
            }
        }
    }
}
</script>




