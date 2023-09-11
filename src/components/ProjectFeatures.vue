<template>
    <div class="projectfeatures">
        <div class="projectcontent">
            <img :src="imgfeatures" alt="Project features"/>
        </div>
    </div>
</template>
<script>
export default 
{
    name:'ProjectFeatures'  ,
    props:
    {
        'imgfeatures':String
    }  
}
</script>
<style>
@media (min-width: 1200px)
{
    .projectsfeatures
    {
        margin-left:auto;
        margin-right:auto;
        width:400px;
        height:400px;
    }
    .projectcontent img
    {
        width:170px;
        height:170px;
        margin:10px;
        border:1px solid #857f7f;
        border-radius: 20px;
    }
}
@media (min-width: 992px) and (max-width: 1199px)
{
    .projectsfeatures
    {
        margin-left:auto;
        margin-right:auto;
        width:400px;
        height:400px;
    }
    .projectcontent img
    {
        width:170px;
        height:170px;
        margin:10px;
        border:1px solid #857f7f;
        border-radius: 20px;
    }
}
@media (min-width: 768px) and (max-width: 991px)
{
    .projectsfeatures
    {
        margin-left:auto;
        margin-right:auto;
        width:400px;
        height:400px;
    }
    .projectcontent img
    {
        width:170px;
        height:170px;
        margin:10px;
        border:1px solid #857f7f;
        border-radius: 20px;
    }
}
@media (min-width: 576px) and (max-width: 767px)
{
    .projectsfeatures
    {
        margin-left:auto;
        margin-right:auto;
        width:400px;
        height:400px;
    }
    .projectcontent img
    {
        width:170px;
        height:170px;
        margin:10px;
        border:1px solid #857f7f;
        border-radius: 20px;
    }
}
@media (max-width: 575px)
{
    .projectsfeatures
    {
        margin-left:auto;
        margin-right:auto;
        width:400px;
        height:400px;
    }
    .projectcontent img
    {
        width:150px;
        height:150px;
        margin:10px;
        border:1px solid #857f7f;
        border-radius: 20px;
    }
}
@media (max-width: 360px)
{
    .projectsfeatures
    {
        margin-left:auto;
        margin-right:auto;
        width:400px;
        height:400px;
    }
    .projectcontent img
    {
        width:120px;
        height:120px;
        margin:10px;
        border:1px solid #857f7f;
        border-radius: 20px;
    }
}
</style>