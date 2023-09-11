<template>
<div class="home">
    <div class="onglet">
        <div class="ongletselect">
            <OngletSelector :onglet1=onglet1 :onglet2=onglet2 :onglet3=onglet3 
                @about=about @technologies=technologies @projects=projects>

            </OngletSelector>
        </div>
        <div class="ongletcontent">
            <Onglet1 v-if="isonglet1">
            
            </Onglet1>
            <Onglet2 v-if="isonglet2">
            
            </Onglet2>
            <Onglet3 v-if="isonglet3">
                
            </Onglet3>
        </div>
    </div>
    <div class="footer">
        <Footer>

        </Footer>
    </div>
</div>

</template>
<script>
let onglet1='About';
let onglet2='Technologies';
let onglet3='Projects';
let isonglet1=false;
let isonglet2=false;
let isonglet3=false;
import OngletSelector from '@/components/OngletSelector.vue'
import Onglet1 from '@/components/Onglet1.vue'
import Onglet2 from '@/components/Onglet2.vue'
import Onglet3 from '@/components/Onglet3.vue'
import Footer from '@/components/Footer.vue'
export default 
{
    name:'Home',
    components:
    {
        OngletSelector,Onglet1,Onglet2,Onglet3,Footer
    },
    mounted:function()
    {
        this.isonglet1=true;
    },
    data()
    {
        return {onglet1,onglet2,onglet3,isonglet1,isonglet2,isonglet3}
    },
    methods:
    {
        about:function()
        {
            this.isonglet1=true;
            this.isonglet2=false;
            this.isonglet3=false;
        },
        technologies:function()
        {
            this.isonglet1=false;
            this.isonglet2=true;
            this.isonglet3=false;
        },
        projects:function()
        {
            this.isonglet1=false;
            this.isonglet2=false;
            this.isonglet3=true;
        }
    }
}
</script>
<style>
.home
{
    margin-left:auto;
    margin-right:auto;
    width:100%;
}
.footer
{
    margin-top:20px;
}
.ongletselect
{
    margin-top:-20px;
}
.ongletcontent
{
    margin-left:auto;
    margin-right:auto;
}
</style>