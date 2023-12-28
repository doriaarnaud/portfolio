<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <div class="headercontent">
      <div class="logo">
        <h1>Hello, I'm</h1>
        <h1>Doria Arnaud</h1>
        <h4>Front-end Web Developer</h4>
      </div>
      <div class="avatar">
        <img src="/profile/Me.png" alt="Avatar" width="200" height="200"/>
      </div>
    </div>
  </header>
  <RouterView />
</template>

<style>
@media (min-width: 1200px)
{
  header
  {
    background-color:#000000;
    height:250px;
    font-family:'Calibri', 'Trebuchet MS', sans-serif;
  }
  .headercontent
  {
    width:80%;
    height:150px;
    margin-left:auto;
    margin-right:auto;
    color:#ffffff;
  }
  .logo
  {
    float:left;
    margin-top:20px;
  }
  .avatar
  {
    float:right;
  }
  .avatar img
  {
    margin-top:20px;
    border-radius:150px;
    border:5px solid #ffffff;
  }
}
@media (min-width: 992px) and (max-width: 1199px)
{
  header
  {
    background-color:#000000;
    height:250px;
    font-family:'Calibri', 'Trebuchet MS', sans-serif;
  }
  .headercontent
  {
    width:80%;
    height:150px;
    margin-left:auto;
    margin-right:auto;
    color:#ffffff;
  }
  .logo
  {
    float:left;
    margin-top:20px;
  }
  .avatar
  {
    float:right;
  }
  .avatar img
  {
    margin-top:20px;
    border-radius:150px;
    border:5px solid #ffffff;
  }
}
@media (min-width: 768px) and (max-width: 991px)
{
  header
  {
    background-color:#000000;
    height:250px;
    font-family:'Calibri', 'Trebuchet MS', sans-serif;
  }
  .headercontent
  {
    width:80%;
    height:150px;
    margin-left:auto;
    margin-right:auto;
    color:#ffffff;
  }
  .logo
  {
    float:left;
    margin-top:20px;
  }
  .avatar
  {
    float:right;
  }
  .avatar img
  {
    margin-top:20px;
    border-radius:150px;
    border:5px solid #ffffff;
  }
}
@media (min-width: 576px) and (max-width: 767px)
{
  header
  {
    background-color:#000000;
    height:250px;
    font-family:'Calibri', 'Trebuchet MS', sans-serif;
  }
  .headercontent
  {
    width:80%;
    height:150px;
    margin-left:auto;
    margin-right:auto;
    color:#ffffff;
  }
  .logo
  {
    float:left;
    margin-top:20px;
  }
  .avatar
  {
    float:right;
  }
  .avatar img
  {
    margin-top:20px;
    border-radius:150px;
    border:5px solid #ffffff;
  }
}
@media (max-width: 575px)
{
  header
  {
    background-color:#000000;
    height:450px;
    font-family:'Calibri', 'Trebuchet MS', sans-serif;
  }
  .headercontent
  {
    width:80%;
    height:150px;
    margin-left:auto;
    margin-right:auto;
    color:#ffffff;
  }
  .logo
  {
    float:right;
    position:absolute;
    top:250px;
    left:10%;
    width:100%;
  }
  .avatar
  {
    float:left;
    margin-left:auto;
    margin-right:auto;
  }
  .avatar img
  {
    margin-top:20px;
    border-radius:150px;
    border:5px solid #ffffff;
  }
}
</style>
