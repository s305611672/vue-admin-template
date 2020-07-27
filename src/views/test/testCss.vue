<template>
  <div style="padding-bottom: 300px">
    <div class="wrap">
      <div class="ribbon">
        <a href="#">New</a>
      </div>
    </div>

    <p class="test-selected"> 我他测试测算出测试他测试测算出测试他测试测算出测试他测试测算出测试他测试测算出测试他测试测算出测试他测试测算出测试他测试测算出测试他测试测算出测试他测试测算出测试他测试测算出测试他测试测算出测试他测试测算出测试他测试测算出测试他测试测算出测试他测试测算出测试他测试测算出测试他测试测算出测试他测试测算出测试
    </p>
    <p> <span class="loading" /></p>
    <div>
      <span class="triangle left" />
      <div class="title">
        标题
      </div>

      <div class="triangle1" />
      <div class="triangle2" />
      <div class="trapezoid" />

      <div class="circle" />
      <div class="ellipse"><div /></div>

      <div class="plus" />
      <div class="target" style="margin-top: 100px;" />

      <div class="gradient" />

      <div class="cup" />
      <p />
      <div class="camera" />

    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style>
html,body {
  font-size: 16px;
}
</style>

<style lang="scss" scoped>
.wrap {
  width: 500px;
  height: 500px;
  overflow: hidden;
  position: relative;
  box-sizing: content-box!important;
  background-color: #f3f3f3;
  margin-top: 100px;
  margin-left: 100px;
}

.ribbon {
  background-color: #f18a31;
  overflow: hidden;
  white-space: nowrap;
  position: absolute;
  /* shadom */
  -webkit-box-shadow: 0 0 10px #888;
  -moz-box-shadow: 0 0 10px #888;
  box-shadow: 0 0 10px #888;
  /* rotate */
  -webkit-transform: rotate(-45deg);
  -moz-transform: rotate(-45deg);
  -ms-transform: rotate(-45deg);
  -o-transform: rotate(-45deg);
  transform: rotate(-45deg);
  /* position */
  left: -50px;
  top: 10px;
}

.ribbon a {
  border: 1px solid #faa;
  color: #fff;
  display: block;
  font: bold 81.25% "Helvetica Neue", Helvetica, Arial, sans-serif;
  margin: 1px 0;
  padding: 5px 60px;
  text-align: center;
  text-decoration: none;
  /* shadow */
  text-shadow: 0 0 5px #444;
}

/** 文字选中样式 */
p.test-selected::selection {
  color: green;
  background-color: pink;
}
p.test-selected::-moz-selection {
  color: green;
  background-color: pink;
}

/* loading效果-简单版 三个点 */
.loading:after {
  display: inline-block;
  overflow: hidden;
  vertical-align: bottom;
  content: "\2026";
  -webkit-animation: ellipsis 2s infinite;
}

@-webkit-keyframes ellipsis {
  from {
    width: 2px;
  }
  to {
    width: 15px;
  }
}

p.test-selected:first-letter {
  float: left;
  color: green;
  font-size: 30px;
}

.triangle {
  /* 基础样式 */
  display: inline-block;
  border: solid 10px transparent;
  width: 0;
  height: 0;
  padding: 0px!important;
  margin: 0;
}
/*下*/
.triangle.bottom {
  border-top-color: black;
}
/*上*/
.triangle.top {
  border-bottom-color: black;
}
/*左*/
.triangle.left {
  border-right-color: black;
}
/*右*/
.triangle.right {
  border-left-color: black;
}

.title {
  font-size: 20px;
  text-align: center;
  color: black;
  position: relative;

  &:before,
  &:after {
    content: " ";
    position: absolute;
    display: block;
    left: 50%;
    top: 50%;
    -webkit-transform: translate3d(-50%, -50%, 0);
    transform: translate3d(-50%, -50%, 0);
    border-top: 1px solid #999;
    width: 20px;
  }
  &:before {
    margin-left: -40px;
  }
  &:after {
    margin-left: 40px;
  }
}

.triangle1 {
  /*锐角三角形*/
  width: 0;
  height: 0;
  border-top: 50px solid transparent;
  border-bottom: 100px solid #249ff1;
  border-left: 30px solid transparent;
  border-right: 100px solid transparent;
}
.triangle2 {
  /*直角三角形*/
  width: 0;
  height: 0;
  border-top: 80px solid transparent;
  border-bottom: 80px solid #ff5b01;
  border-left: 50px solid #ff5b01;
  border-right: 50px solid transparent;
}
.trapezoid {
  /*梯形*/
  width: 0;
  height: 0;
  border-top: none;
  border-right: 80px solid transparent;
  border-bottom: 60px solid #13dbed;
  border-left: 80px solid #13dbed;
}

.circle,
.ellipse {
  width: 100px;
  height: 100px;
  background: #249ff1;
  border-radius: 50%;
}
.ellipse {
  width: 150px;
  background: #ff9e01;
}

.plus {
  width: 60px;
  height: 60px;
  margin-left: 50px; /*由于box-shadow不占空间，常常需要添加margin来校正位置*/
  background: #888;
  box-shadow: 0 -30px 10px green, 0 30px 1px  blue, -30px 0 0 red, 60px 0 0 6px yellow;
}
.target {
  width: 30px;
  height: 30px;
  background: red;
  border-radius: 50%;
  margin-left: 50px;
  box-shadow: 0 0 0 10px #fff, 0 0 0 20px red, 0 0 0 30px #fff, 0 0 0 40px red;
}

.gradient {
  position: relative;
  width: 300px;
  height: 300px;
  // border-radius: 50%;
  background-color: silver;
  background-image: linear-gradient(335deg, #b00 23px, transparent 23px),
    linear-gradient(155deg, #d00 23px, transparent 23px), linear-gradient(
      335deg,
      #b00 23px,
      transparent 23px
    ), linear-gradient(155deg, #d00 23px, transparent 23px);
  background-size: 58px 58px;
  background-position: 0px 2px, 4px 35px, 29px 31px, 34px 6px;
  background-repeat: no-repeat;
}

.cup {
  display: inline-block;
  width: 0.9em;
  height: 0.4em;
  border: 0.25em solid;
  border-bottom: 1.1em solid;
  border-radius: 0 0 0.25em 0.25em;
}
.cup:before {
  position: absolute;
  right: -0.6em;
  top: 0;
  width: 0.3em;
  height: 0.8em;
  border: 0.25em solid;
  border-left: none;
  border-radius: 0 0.25em 0.25em 0;
  content: "";
}

.camera {
  display: inline-block;
  border-style: solid;
  border-width: 0.65em 0.9em;
  border-radius: 0.1em;
}
.camera:before {
  position: absolute;
  top: -0.3em;
  left: -0.3em;
  width: 0.4em;
  height: 0.4em;
  border-radius: 50%;
  border: 0.1em solid #fff;
  box-shadow: 0 0 0 0.08em, 0 0 0 0.16em #fff;
  content: "";
}
.camera:after {
  position: absolute;
  top: -0.5em;
  left: 0.5em;
  width: 0.2em;
  border-top: 0.125em solid #fff;
  content: "";
}
</style>
