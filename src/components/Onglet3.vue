<template>
    <div class="onglet3">
        <div class="onglet3content">
            <div class="projects" v-for="project in tabproject" :key="project.id">
                <a href="#features">
                    <img :src="project.thumb" alt="Vue3 projects" width="350" height="250" :title="project.ads" 
                    @click="details(project.id)"/>
                </a> 
                <div class="thumbtitle">
                    <h2>{{ project.title }}</h2>
                    <a :href="project.link" :title="project.link" target="blank">Visit project</a>
                </div>
            </div>
            <div class="gamingdetails">
                <h3 id="features">Project features</h3>
                <div class="gamingcontent" v-if="isgaming">
                    <ProjectFeatures v-for="(item,id) in gamingtab" :key="id" :imgfeatures="item">
                        
                    </ProjectFeatures>
                </div>
                <div class="toecontent" v-if="istoe">
                    <ProjectFeatures v-for="(item,id) in tictab" :key="id" :imgfeatures="item">
                        
                    </ProjectFeatures>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import ProjectFeatures from '@/components/ProjectFeatures.vue'
let isgaming=false;
let istoe=false;
let tabproject=
[
    {id:0,thumb:'/projects/gaming.jpg',title:'Gaming Shop',link:"https://gamingshop-eta.vercel.app/",ads:'See project features'},
    {id:1,thumb:'/projects/tictactoe.JPG',title:'Tic-Tac-Toe Game',link:"https://tictactoe-five-neon.vercel.app/",ads:'See project features'}
];
let gamingtab=
[
    '/projects/gamingshop_features/1.jpg',
    '/projects/gamingshop_features/2.png',
    '/projects/gamingshop_features/3.png',
    '/projects/gamingshop_features/4.png'
];
let tictab=
[
    '/projects/tictactoe_features/1.png',
    '/projects/tictactoe_features/2.png',
    '/projects/tictactoe_features/3.png',
    '/projects/tictactoe_features/4.png'
];
export default 
{
    name:'Onglet3',
    data()
    {
        return {tabproject,gamingtab,tictab,isgaming,istoe}
    },
    components:
    {
        ProjectFeatures
    },
    mounted:function()
    {
        this.isgaming=true;
    },
    methods:
    {
        details:function(id)
        {
            switch(id)
            {
                case 0:
                    this.isgaming=true;
                    this.istoe=false;
                    break;
                case 1:
                    this.isgaming=false;
                    this.istoe=true;
                    break;
            }
        }
    }
}
</script>
<style>
@media (min-width: 1200px)
{
    .onglet3
    {
        margin-top:0px;
        border:1px solid #000000;
    }
    .onglet3content
    {
        position:relative;
		border-top:5px solid black;
        width:100%;
        height:600px;
        margin-right:auto;
        padding-top:10px;
        background-color: #ffffff;
        display:flex;
        flex-wrap: wrap;
        align-content: center;
        font-family: 'Segoe UI', Tahoma, Verdana, sans-serif;
    }
    .projects
    {
        width:300px;
        margin-left:20px;
        margin-right:20px;
        text-align: center;
		background-color:#f0f0f0;
        border-radius:10px;
        padding:5px;
    }
    .projects a
    {
        text-decoration:none;
        font-family:'Segoe UI', Tahoma, Verdana, sans-serif;
        color:#000000;
        font-size:1.5em;
    }
    .projects a:hover
    {
        text-decoration: underline;
        color:#00aa00;
    }
    .projects img
    {
        width:280px;
        border:1px solid #000000;
        border-radius:10px;
        padding:5px;
    }
    .projects img:hover
    {
        cursor:pointer;
    }
    .projects:hover
    {
        box-shadow:5px 5px 5px 5px #c2bdbd;
    }
    .thumbtitle
    {
        font-size:0.8em;
    }
    .gamingdetails
    {
        position:absolute;
		margin-left:auto;
		margin-right:auto;
        float:right;
        margin-top:25px;
        right:50px;
        width:450px;
        height:450px;
        border:1px solid black;
    }
	.gamingdetails h3
	{
		margin-left:10px;
	}
    .gamingcontent
    {
        display:flex;
        flex-wrap: wrap;
        justify-content: center;
    }
    .toecontent
    {
        display:flex;
        flex-wrap: wrap;
        justify-content: center;
    }
    
}
@media (min-width: 992px) and (max-width: 1199px)
{
    .onglet3
    {
        margin-top:0px;
        border:1px solid #000000;
    }
    .onglet3content
    {
		border-top:5px solid black;
        position:relative;
        width:100%;
        height:500px;
        margin-left:0;
        margin-right:auto;
        padding-top:10px;
        background-color: #ffffff;
        display:flex;
        flex-wrap: wrap;
        align-content: center;
        font-family: 'Segoe UI', Tahoma, Verdana, sans-serif;
    }
    .projects
    {
        width:200px;
        margin-left:20px;
        margin-right:20px;
        text-align: center;
		background-color:#f0f0f0;
        border-radius:10px;
        padding:5px;
    }
	.projects a
    {
        text-decoration:none;
        font-family:'Segoe UI', Tahoma, Verdana, sans-serif;
        color:#000000;
        font-size:1.5em;
    }
    .projects a:hover
    {
        text-decoration: underline;
        color:#009900;
    }
    .projects img
    {
        width:170px;
        height:200px;
        background-color:#f0f0f0;
        border-radius:10px;
        padding:5px;
    }
    .projects:hover
    {
        box-shadow:5px 5px 5px 5px #c2bdbd;
    }
    .thumbtitle
    {
        font-size:0.8em;
    }
    .gamingdetails
    {
        position:absolute;
		margin-left:auto;
		margin-right:auto;
        float:right;
        margin-top:30px;
        left:520px;
        width:450px;
        height:450px;
        border:1px solid black;
    }
	.gamingdetails h3
	{
		margin-left:10px;
	}
    .gamingcontent
    {
        display:flex;
        flex-wrap: wrap;
        justify-content: center;
    }
    .toecontent
    {
        display:flex;
        flex-wrap: wrap;
        justify-content: center;
    }
}
@media (min-width: 768px) and (max-width: 991px)
{
    .onglet3
    {
        margin-top:0px;
        border:1px solid #000000;
    }
    .onglet3content
    {
		border-top:5px solid black;
        position:relative;
        width:100%;
        height:1250px;
        margin-left:0;
        margin-right:auto;
        padding-top:10px;
        background-color: #ffffff;
        display:flex;
        flex-wrap: wrap;
        align-content:flex-start;
        font-family: 'Segoe UI', Tahoma, Verdana, sans-serif;
    }
    .projects
    {
        width:100%;
		height:360px;
        margin-left:20px;
        margin-right:20px;
        margin-top:10px;
        text-align: center;
		background-color:#f0f0f0;
        border-radius:10px;
        padding:5px;
    }
    .projects img
    {
        width:300px;
        border:1px solid #000000;
        border-radius:10px;
        padding:5px;
    }
	.projects a
    {
		font-weight:bold;
        text-decoration:none;
        font-family:'Segoe UI', Tahoma, Verdana, sans-serif;
        color:#000000;
        font-size:1.5em;
    }
    .projects a:hover
    {
        text-decoration: underline;
        color:#009900;
    }
    .projects:hover
    {
        box-shadow:5px 5px 5px 5px #c2bdbd;
    }
    .thumbtitle
    {
        font-size:0.8em;
    }
    .gamingdetails
    {
		margin-left:auto;
		margin-right:auto;
        margin-top:30px;
        width:500px;
        height:450px;
        border:1px solid black;
    }
	.gamingdetails h3
	{
		margin-left:10px;
	}
    .gamingcontent
    {
        display:flex;
        flex-wrap: wrap;
        justify-content: center;
    }
    .toecontent
    {
        display:flex;
        flex-wrap: wrap;
        justify-content: center;
    }
}
@media (min-width: 576px) and (max-width: 767px)
{
    .onglet3
    {
        margin-top:0px;
        border:1px solid #000000;
    }
    .onglet3content
    {
		border-top:5px solid black;
        position:relative;
        width:100%;
        height:1300px;
        margin-left:0;
        margin-right:auto;
        padding-top:0px;
        background-color: #ffffff;
        display:flex;
        flex-wrap: wrap;
        align-content: center;
        font-family: 'Segoe UI', Tahoma, Verdana, sans-serif;
    }
    .projects
    {
        width:100%;
		height:360px;
        margin-left:40px;
        margin-right:40px;
        margin-top:10px;
        text-align: center;
        border-radius:10px;
		background-color:#f0f0f0;
        padding:5px;
    }
	.projects a
    {
		font-weight:bold;
        text-decoration:none;
        font-family:'Segoe UI', Tahoma, Verdana, sans-serif;
        color:#000000;
        font-size:1.5em;
    }
    .projects a:hover
    {
        text-decoration: underline;
        color:#009900;
    }
    .projects img
    {
        width:300px;
        border:2px solid #000000;
        border-radius:10px;
        padding:5px;
    }
    .projects:hover
    {
        box-shadow:5px 5px 5px 5px #c2bdbd;
    }
    .thumbtitle
    {
        font-size:0.8em;
    }
    .gamingdetails
    {
		margin-left:auto;
		margin-right:auto;
        margin-top:30px;
        width:500px;
        height:450px;
        border:1px solid black;
    }
	.gamingdetails h3
	{
		margin-left:10px;
	}
    .gamingcontent
    {
        display:flex;
        flex-wrap: wrap;
        justify-content: center;
    }
    .toecontent
    {
        display:flex;
        flex-wrap: wrap;
        justify-content: center;
    }
}
@media (max-width: 575px)
{
    .onglet3
    {
        margin-top:0px;
        border:1px solid #000000;
    }
    .onglet3content
    {
		border-top:5px solid black;
        position:relative;
        width:100%;
        height:1200px;
        margin-left:0;
        margin-right:auto;
        padding-top:20px;
        background-color: #ffffff;
        display:flex;
        flex-wrap: wrap;
        align-content: center;
        font-family: 'Segoe UI', Tahoma, Verdana, sans-serif;
    }
    .projects
    {
        width:100%;
        margin-left:20px;
        margin-right:20px;
        margin-top:10px;
        text-align: center;
        background-color:#f0f0f0;
        border-radius:10px;
        padding:5px;
    }
	.projects a
    {
		font-weight:bold;
        text-decoration:none;
        font-family:'Segoe UI', Tahoma, Verdana, sans-serif;
        color:#000000;
        font-size:1.5em;
    }
    .projects a:hover
    {
        text-decoration: underline;
        color:#009900;
    }
    .projects img
    {
        width:100%;
    }
    .projects img:hover
    {
        cursor:pointer;
    }
    .projects:hover
    {
        box-shadow:5px 5px 5px 5px #c2bdbd;
    }
    .thumbtitle
    {
        font-size:0.5em;
    }
	.gamingdetails
    {
		margin-left:auto;
		margin-right:auto;
        margin-top:30px;
        width:450px;
        height:450px;
    }
    .gamingdetails h3
    {
        margin-left:10px;
    }
    .gamingcontent
    {
        display:flex;
        flex-wrap: wrap;
        justify-content: center;
    }
    .toecontent
    {
        display:flex;
        flex-wrap: wrap;
        justify-content: center;
    }
    .projects a
    {
        text-decoration:none;
        font-family:'Segoe UI', Tahoma, Verdana, sans-serif;
        color:#000000;
        font-size:2em;
    }
    .projects a:hover
    {
        text-decoration: underline;
        color:#0000ff;
    }
}
@media (max-width: 350px)
{
    .onglet3
    {
        margin-top:0px;
        border:1px solid #000000;
    }
    .onglet3content
    {
		border-top:5px solid black;
        position:relative;
        width:100%;
        height:1200px;
        margin-left:0;
        margin-right:auto;
        padding-top:20px;
        background-color: #ffffff;
        display:flex;
        flex-wrap: wrap;
        align-content: center;
        font-family: 'Segoe UI', Tahoma, Verdana, sans-serif;
    }
    .projects
    {
        width:100%;
        margin-left:20px;
        margin-right:20px;
        margin-top:10px;
        text-align: center;
        background-color:#f0f0f0;
        border-radius:10px;
        padding:5px;
    }
    .projects img
    {
        width:100%;
    }
    .projects img:hover
    {
        cursor:pointer;
    }
    .projects:hover
    {
        box-shadow:5px 5px 5px 5px #c2bdbd;
    }
    .thumbtitle
    {
        font-size:0.5em;
    }
	.gamingdetails
    {
		margin-left:auto;
		margin-right:auto;
        margin-top:30px;
        width:300px;
        height:400px;
        border:1px solid black;
    }
    .gamingdetails h3
    {
        margin-left:10px;
    }
    .gamingcontent
    {
        display:flex;
        flex-wrap: wrap;
        justify-content: center;
    }
    .toecontent
    {
        display:flex;
        flex-wrap: wrap;
        justify-content: center;
    }
    .projects a
    {
        text-decoration:none;
        font-family:'Segoe UI', Tahoma, Verdana, sans-serif;
        color:#000000;
        font-size:2em;
    }
    .projects a:hover
    {
        text-decoration: underline;
        color:#009900;
    }
}
</style>
