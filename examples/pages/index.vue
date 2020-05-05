<template>
  <div class="pg-index">
    <div class="index-container">
      <img src="../assets/img/logo.png"
           class="animated bounceInDown">
      <p class="animated bounceInDown">一款轻量级、模块化的前端 UI 组件库</p>
    </div>
    <div class="separate-panel">
      <div class="about">
        <router-link :to="{name: 'giud'}">开始使用</router-link>
        <a target="_blank"
           class="btn-github"
           href="https://github.com/VV-UI/VV-UI">GitHub</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      height: document.documentElement.clientHeight
    }
  }
}
</script>
<style type="text/less" lang="less">
.pg-index {
  .index-container {
    width: 960px;
    margin: 0 auto;
    text-align: center;
    padding: 100px 0;
    p {
      margin-top: 56px;
      // color: #8994c6;
      color: #99816d;
      font-size: 32px;
    }
  }
  .separate-panel {
    position: relative;
    .about {
      position: absolute;
      width: 100%;
      height: 200px;
      top: 20px;
      z-index: 9;
      background: #fff;
      text-align: center;
      a {
        background: #99816d !important;
        color: #fff;
        background-image: linear-gradient(90deg, #00aeff 0%, #99816d 100%);
        box-shadow: 0 2px 6px 0 #99816d;
        display: inline-block;
        width: 190px;
        height: 56px;
        margin: 0 35px;
        font-size: 18px;
        line-height: 56px;
        border-radius: 28px;
        transition: all 0.3s;
        cursor: pointer;
      }
      a:hover {
        transform: scale(1.5);
      }
      .btn-github {
        // color: #316de9;
        border: 1px solid #99816d;
        box-shadow: 0 2px 6px 0 #99816d;
        background: #fff;
        // box-shadow: none;
      }
    }
  }
  .separate-panel:after {
    content: "";
    display: block;
    position: absolute;
    top: -80px;
    width: 100%;
    height: 250px;
    background: #fff;
    box-shadow: 0 -4px 30px 0 #dfe1e6;
    transform: skewY(-4deg);
  }
}
</style>
