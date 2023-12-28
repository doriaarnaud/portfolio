<template>
    <div class="ongletselector">
        <div class="ongletselectorcontent">
            <button id="onglet1" 
                :class="[{onglet1normal:isonglet1normal,onglet1selected:isonglet1selected}]" 
                @click="$emit('about')" @mouseup="onglet1class">{{ onglet1 }}
            </button>
            <button id="onglet2" 
                :class="[{onglet2normal:isonglet2normal,onglet2selected:isonglet2selected}]" 
                @click="$emit('technologies')" @mouseup="onglet2class">{{ onglet2 }}
            </button>
            <button id="onglet3" 
                :class="[{onglet3normal:isonglet3normal,onglet3selected:isonglet3selected}]" 
                @click="$emit('projects')" @mouseup="onglet3class">{{ onglet3 }}
            </button>
        </div>
    </div>
</template>
<script>
let isonglet1selected=false;
let isonglet2selected=false;
let isonglet3selected=false;
let isonglet1normal=false;
let isonglet2normal=false;
let isonglet3normal=false;
export default 
{
    name:'OngletSelector',
    props:
    {
        'onglet1':String,
        'onglet2':String,
        'onglet3':String
    },
    data()
    {
        return {isonglet1selected,isonglet2selected,isonglet3selected,
            isonglet1normal,isonglet2normal,isonglet3normal}
    },
    mounted:function()
    {
        this.isonglet1selected=true;
        this.isonglet2selected=false;
        this.isonglet3selected=false;
        this.isonglet1normal=false;
        this.isonglet2normal=true;
        this.isonglet3normal=true;
    },  
    methods:
    {
        onglet1class:function()
        {
            this.isonglet1selected=true;
            this.isonglet2selected=false;
            this.isonglet3selected=false;
            this.isonglet1normal=false;
            this.isonglet2normal=true;
            this.isonglet3normal=true;
        },
        onglet2class:function()
        {
            this.isonglet1selected=false;
            this.isonglet2selected=true;
            this.isonglet3selected=false;
            this.isonglet1normal=true;
            this.isonglet2normal=false;
            this.isonglet3normal=true;
        },
        onglet3class:function()
        {
            this.isonglet1selected=false;
            this.isonglet2selected=false;
            this.isonglet3selected=true;
            this.isonglet1normal=true;
            this.isonglet2normal=true;
            this.isonglet3normal=false;
        }
    }
}
</script>
<style>
@media (min-width: 1200px)
{
    .ongletselector
    {
        margin-left:0;
        margin-top:40px;
    }
    .ongletselectorcontent button
    {
        width:150px;
        height: 50px;
        font-size:1.2em;
        padding:0;
        font-family:'Franklin Gothic Medium', 'Arial Narrow', 'Arial', 'sans-serif';
        margin-left:5px;
        margin-right: 5px;
        margin-bottom: -2px;
    }
    button#onglet1:hover
    {
        cursor:pointer;
    }
    button#onglet2:hover
    {
        cursor:pointer;
    }
    button#onglet3:hover
    {
        cursor:pointer;
    }
    button#onglet1,button#onglet2,button#onglet3
    {
        border-radius: 10px 10px 0px 0px;
		border:1px solid black;
    }
    .onglet1normal
    {
        background-color: #ffffff;
        color:#000000;
    }
    .onglet2normal
    {
        background-color: #ffffff;
        color:#000000;
    }
    .onglet3normal
    {
        background-color: #ffffff;
        color:#000000;
    }
    .onglet1selected
    {
        background-color: #000000;
		border-bottom:none;
        color:#ffffff;
    }
    .onglet2selected
    {
        background-color: #000000;
        border-bottom:none;
        color:#ffffff;
    }
    .onglet3selected
    {
        background-color: #000000;
        border-bottom:none;
        color:#ffffff;
    }
}
@media (min-width: 992px) and (max-width: 1199px)
{
    .ongletselector
    {
        margin-left:0;
        margin-top:40px;
    }
    .ongletselectorcontent button
    {
        width:150px;
        height: 50px;
        font-size:1.2em;
        padding:0;
        font-family:'Franklin Gothic Medium', 'Arial Narrow', 'Arial', 'sans-serif';
        margin-left:5px;
        margin-right: 5px;
        margin-bottom: -2px;
    }
    button#onglet1:hover
    {
        cursor:pointer;
    }
    button#onglet2:hover
    {
        cursor:pointer;
    }
    button#onglet3:hover
    {
        cursor:pointer;
    }
    button#onglet1,button#onglet2,button#onglet3
    {
        border-radius: 10px 10px 0px 0px;
		border:1px solid black;
    }
    .onglet1normal
    {
        background-color: #ffffff;
        color:#000000;
    }
    .onglet2normal
    {
        background-color: #ffffff;
        color:#000000;
    }
    .onglet3normal
    {
        background-color: #ffffff;
        color:#000000;
    }
    .onglet1selected
    {
        background-color: #000000;
		border-bottom:none;
        color:#ffffff;
    }
    .onglet2selected
    {
        background-color: #000000;
        border-bottom:none;
        color:#ffffff;
    }
    .onglet3selected
    {
        background-color: #000000;
        border-bottom:none;
        color:#ffffff;
    }
}
@media (min-width: 768px) and (max-width: 991px)
{
    .ongletselector
    {
        margin-left:0;
        margin-top:40px;
    }
    .ongletselectorcontent button
    {
        width:150px;
        height: 50px;
        font-size:1.2em;
        padding:0;
        font-family:'Franklin Gothic Medium', 'Arial Narrow', 'Arial', 'sans-serif';
        margin-left:5px;
        margin-right: 5px;
        margin-bottom: -2px;
    }
    button#onglet1:hover
    {
        cursor:pointer;
    }
    button#onglet2:hover
    {
        cursor:pointer;
    }
    button#onglet3:hover
    {
        cursor:pointer;
    }
    button#onglet1,button#onglet2,button#onglet3
    {
        border-radius: 10px 10px 0px 0px;
		border:1px solid black;
    }
    .onglet1normal
    {
        background-color: #ffffff;
        color:#000000;
    }
    .onglet2normal
    {
        background-color: #ffffff;
        color:#000000;
    }
    .onglet3normal
    {
        background-color: #ffffff;
        color:#000000;
    }
    .onglet1selected
    {
        background-color: #000000;
		border-bottom:none;
        color:#ffffff;
    }
    .onglet2selected
    {
        background-color: #000000;
        border-bottom:none;
        color:#ffffff;
    }
    .onglet3selected
    {
        background-color: #000000;
        border-bottom:none;
        color:#ffffff;
    }
}
@media (min-width: 576px) and (max-width: 767px)
{
    .ongletselector
    {
        margin-left:0;
        margin-top:40px;
    }
    .ongletselectorcontent button
    {
        width:150px;
        height: 50px;
        font-size:1.2em;
        padding:0;
        font-family:'Franklin Gothic Medium', 'Arial Narrow', 'Arial', 'sans-serif';
        margin-left:5px;
        margin-right: 5px;
        margin-bottom: -2px;
    }
    button#onglet1:hover
    {
        cursor:pointer;
    }
    button#onglet2:hover
    {
        cursor:pointer;
    }
    button#onglet3:hover
    {
        cursor:pointer;
    }
    button#onglet1,button#onglet2,button#onglet3
    {
        border-radius: 10px 10px 0px 0px;
		border:1px solid black;
    }
    .onglet1normal
    {
        background-color: #ffffff;
        color:#000000;
    }
    .onglet2normal
    {
        background-color: #ffffff;
        color:#000000;
    }
    .onglet3normal
    {
        background-color: #ffffff;
        color:#000000;
    }
    .onglet1selected
    {
        background-color: #000000;
		border-bottom:none;
        color:#ffffff;
    }
    .onglet2selected
    {
        background-color: #000000;
        border-bottom:none;
        color:#ffffff;
    }
    .onglet3selected
    {
        background-color: #000000;
        border-bottom:none;
        color:#ffffff;
    }
}
@media (max-width: 575px)
{
    .ongletselector
    {
        margin-left:0;
        margin-top:40px;
    }
    .ongletselectorcontent button
    {
        width:100px;
        height: 50px;
        font-size:1em;
        padding:0;
        font-family:'Franklin Gothic Medium', 'Arial Narrow', 'Arial', 'sans-serif';
        margin-left:5px;
        margin-right: 5px;
        margin-bottom: -2px;
    }
    button#onglet1:hover
    {
        cursor:pointer;
    }
    button#onglet2:hover
    {
        cursor:pointer;
    }
    button#onglet3:hover
    {
        cursor:pointer;
    }
    button#onglet1,button#onglet2,button#onglet3
    {
        border-radius: 10px 10px 0px 0px;
		border:1px solid black;
    }
    .onglet1normal
    {
        background-color: #ffffff;
        color:#000000;
    }
    .onglet2normal
    {
        background-color: #ffffff;
        color:#000000;
    }
    .onglet3normal
    {
        background-color: #ffffff;
        color:#000000;
    }
    .onglet1selected
    {
        background-color: #000000;
		border-bottom:none;
        color:#ffffff;
    }
    .onglet2selected
    {
        background-color: #000000;
        border-bottom:none;
        color:#ffffff;
    }
    .onglet3selected
    {
        background-color: #000000;
        border-bottom:none;
        color:#ffffff;
    }
}
@media (max-width: 350px)
{
    .ongletselector
    {
        margin-left:0;
        margin-top:40px;
    }
    .ongletselectorcontent button
    {
        width:60px;
        height: 50px;
        font-size:0.7em;
        padding:0;
        font-family:'Franklin Gothic Medium', 'Arial Narrow', 'Arial', 'sans-serif';
        margin-left:5px;
        margin-right: 5px;
        margin-bottom: -2px;
    }
    button#onglet1:hover
    {
        cursor:pointer;
    }
    button#onglet2:hover
    {
        cursor:pointer;
    }
    button#onglet3:hover
    {
        cursor:pointer;
    }
    button#onglet1,button#onglet2,button#onglet3
    {
        border-radius: 10px 10px 0px 0px;
		border:1px solid black;
    }
    .onglet1normal
    {
        background-color: #ffffff;
        color:#000000;
    }
    .onglet2normal
    {
        background-color: #ffffff;
        color:#000000;
    }
    .onglet3normal
    {
        background-color: #ffffff;
        color:#000000;
    }
    .onglet1selected
    {
        background-color: #000000;
		border-bottom:none;
        color:#ffffff;
    }
    .onglet2selected
    {
        background-color: #000000;
        border-bottom:none;
        color:#ffffff;
    }
    .onglet3selected
    {
        background-color: #000000;
        border-bottom:none;
        color:#ffffff;
    }
}
</style>