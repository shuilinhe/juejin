<template>
  <article class="dakuai">
    <div>
      <h1 class="datitle">前端怎么样限制用户截图？</h1>
      <div>
        <img class=user_header src="../img/users_img/1.jpeg">
        <div class="xiaozi">
          <div>
            <span class="username">正经程序员</span>
            <img class="dengji" src="../img/users_img/等级.png">
            <img src="../img/users_img/vip等级.svg">
          </div>
          <div class="time">2022年08月04日 09:39 · 阅读224</div>
        </div>
        <button class="guanzhu"><span>＋</span><span>关注</span></button>
      </div>
    </div>
    <img class="datu" src="../img/users_img/封面.webp">
    <div class="markdown">
      <p>
        携手创作，共同成长！这是我参与「掘金日新计划 · 8 月更文挑战」的第3天，<a class="huodong" src="https://juejin.cn/post/7123120819437322247">点击查看活动详情</a>
      </p>
      <p style="height:52.5px ;">
        做后台系统，或者版权比较重视的项目时，产品经常会提出这样的需求：能不能禁止用户截图？有经验的开发不会直接拒绝产品，而是进行引导。
      </p>
      <p style="height:52.5px ;">
        先了解初始需求是什么？是内容数据过于敏感，严禁泄漏。还是内容泄漏后，需要溯源追责。不同的需求需要的方案也不同。来看看就限制用户截图，有哪些脑洞？
      </p>
      <div id="block1">
        <h1 class="p_h1" id="heading-0">有哪些脑洞</h1>
        <p>v站和某乎上的大佬给出了不少脑洞，我又加了点思路。</p>
      </div>
      <div id="block2">
        <h2 class="p_h2" id="heading-1">1.基础方案，阻止右键保存和拖拽</h2>
        <p style="height:52.5px ;">这个方案是最基础，当前可只能阻拦一些小白用户。如果是浏览器，分分钟调出控制台，直接找到图片url。还可以直接ctrl+p，进入打印模式，直接保存下来再裁减。</p>
      </div>
      <div id="block3">
        <h2 class="p_h2" id="heading-2">2.失焦后加遮罩层</h2>
        <p style="height:52.5px ;">
          这个方案有点意思，看敏感信息时，必须鼠标点在某个按钮上，照片才完整显示。如果失去焦点图片显示不完整或者直接遮罩盖住。
        </p>
      </div>
      <div id="block4">
        <h2 class="p_h2" id="heading-3">3.高速动态马赛克</h2>
        <p style="height:105px ;">
          这个方案是可行的，并且在一些网站已经得到了应用，在视频或者图片上随机插像素点，动态跑来跑去，对客户来说，每一时刻屏幕上显示的都是完整的图像，靠用户的视觉残留看图或者视频。即时手机拍照也拍不完全。实际应用需要优化的点还是挺多的。比如用手机录像就可以看到完整内容，只是增加了截图成本。
        </p>
        <p>下面是一个知乎上的方案效果。（<a class="huodong" src="https://link.juejin.cn/?target=https%3A%2F%2Fwww.zhihu.com%2Fquestion%2F417108591%2Fanswer%2F1450568587">原地址</a>）：</p>
        <img style="width:610px;height: 751px; " src="../img/users_img/pp.webp">
      </div>
      <div id="block5">
        <h1 class="p_h1" id="heading-4" >正经需求vs方案</h1>
        <p style="height:52.5px ;">
          其实限制用户截图这个方案本身就不合理，除非整个设备都是定制的，在软件上阉割截图功能。为了这个需求添加更复杂的功能对于一些安全性没那么高的需求来说，有点本末倒置了。
        </p>
        <p>下面聊聊正经方案：</p>
        <p style="height:52.5px ;">1.对于后台系统敏感数据或者图片，主要是担心泄漏出去，可以采用斜45度七彩水印，想要完全去掉几乎不可能，就是观感比较差。</p>
        <p style="height:52.5px ;">2.对于图片版权，可以使用现在主流的盲水印，之前看过腾讯云提供的服务，当然成本比较高，如果版权需求较大，使用起来效果比较好。</p>
        <p style="height:80px ;">3.视频方案，tiktok下载下来的时候会有一个水印跑来跑去，当然这个是经过处理过的视频，非原画，画质损耗也比较高。Netflix等视频网站采用的是服务端权限控制，走的视频流，每次播放下载加密视频，同时获得短期许可，得到许可后在本地解密并播放，一旦停止播放后许可失效。</p>
        <p style="height:52.5px ;">总之，除了类似于Android提供的截图API等底层功能，其他的功能实现都不完美。即使是底层控制了，一样可以拍照录像，没有完美的方案。不过还是可以做的相对安全。</p>
        <p class="p_jiewei">你还有什么新思路吗？有的话咱评论区见，欢迎点赞收藏关注，感谢！</p>
      </div>
    </div>
    <div>
      <div class="tab_title">分类：</div><a class="fenlei" href="#"><span>前端</span></a>
      <div class="tab_title" style="margin-left:40px ;">标签：</div>
      <a class="biaoqian" href="#"><span>安全</span></a>
      <a style="width:66.229px ;" class="biaoqian" href="#"><span> JavaScript</span></a>
      <a class="biaoqian" href="#"><span>前端</span></a>
    </div>

  </article>


</template>

<script>
export default {
  name: "Content"

}


</script>

<style>
.dakuan{
  width: 1140px;
  height: 6854.3px;
  padding-bottom: 96px;
  margin-top: 21.204px;
  background-color:#F2F2F2 ;
  position: relative;
  left:270px;
  top:50px;


}

article{
  width: 755.920px;
  height: 2730.736px;
  padding: 32.040px 32.040px 39.960px 32.040px;
  background-color: white;
  /* margin-top: 100px; */

}

.datitle{
  color: rgb(37,41,51);
  display: block;
  font-size: 32.004px;
  font-weight: 600;
  font-family: -apple-system, system-ui, "Segoe UI", Roboto, Ubuntu, Cantarell, "Noto Sans", sans-serif, BlinkMacSystemFont, "Helvetica Neue", "PingFang SC", "Hiragino Sans GB", "Microsoft YaHei", Arial
;
  margin-bottom: 25px;
}
.user_header{
  width: 39.99px;
  height: 39.99px;
  margin-right: 12px;
  background-color: rgb(238,238,238);
  background-position-x: 50%;
  background-position-y: 50%;
  border-radius: 50%;
  float: left;
}

.dengji{
  width: 35px;
  height: 16px;
}
.xiaozi{
  float: left;
}
.username{
  margin-top: -5px;
  float: left;
  color: rgb(81,87,103);
  display: block;
  width: 79.969px;
  height: 24px;
  line-height: 24px;
  font-size: 15.996px;
  font-family: -apple-system, system-ui, "Segoe UI", Roboto, Ubuntu, Cantarell, "Noto Sans", sans-serif, BlinkMacSystemFont, "Helvetica Neue", "PingFang SC", "Hiragino Sans GB", "Microsoft YaHei", Arial;
}
.time{
  color: rgb(138,145,159);
  width: 400px;
  height: auto;
  font-size: 14.004px;
  letter-spacing: 1px;
  line-height: 22px;
  float: left;
  margin-top: 2px;

}

.guanzhu{
  display: flex;
  width: 68px;
  height: 32px;
  padding: 0 12px;
  border: 1px rgba(30,128,255,0.3) solid;
  border-radius: 4px;
  color: rgb(30,128,255);
  background-color: rgba(30,128,255,0.05);
  float:right;
  font-size: 14px;
  line-height: 32px;
}

.datu{
  width: 755.938px;
  height: 425.458px;
  margin-top: 20px;
}
.huodong{
  border-bottom: 1px rgb(145,109,213) solid;
  color:rgb(145,109,213);
  font-weight: bolder;
  font-size: 15px;
  font-family: -apple-system-font, BlinkMacSystemFont, "Helvetica Neue", "PingFang SC", "Hiragino Sans GB", "Microsoft YaHei UI", "Microsoft YaHei", Arial, sans-serif
;
}

p{
  color: rgb(51,51,51);
  display: block;
  font-size: 15px;
  letter-spacing: 2px;
  line-height: 26.25px;
  width: 755.938px;
  height: 26.250px;
  margin: 22px 0;
  font-family: -apple-system-font, BlinkMacSystemFont, "Helvetica Neue", "PingFang SC", "Hiragino Sans GB", "Microsoft YaHei UI", "Microsoft YaHei", Arial, sans-serif
;
  font-weight: 400;

}
.p_h1{
  display: block;
  border-left: 5px rgb(119,48,152) solid;
  color: rgb(51,51,51);
  width: 706.229px;
  height: 40.250px;
  padding-left: 10px;
  margin-top: 15.410px;
  margin-bottom: 5px;
  font-size: 23px;
  font-family: -apple-system-font,BlinkMacSystemFont,Helvetica Neue,PingFang SC,Hiragino Sans GB,Microsoft YaHei UI,Microsoft YaHei,Arial,sans-serif;
  font-weight: bolder;
  letter-spacing: 2px;
  line-height: 40.25px;
}

.p_h2{
  display: block;
  width: 721.229px;
  height: 29.750px;
  border-left: 5px rgb(216,156,246) solid;
  margin: 17px 0;
  padding-left: 10px;
  color: rgb(51,51,51);
  font-size: 17px;
  font-weight: bolder;
  letter-spacing: 2px;
  line-height: 29.75px;
}

.p_jiewei{
  color: rgb(145,109,213);
  font-size: 15px;
  font-weight: bolder;
  letter-spacing: 2px;
}
.p_jiewei::after{
  content: "」";
}
.p_jiewei::before{
  content: "「";
}

.fenlei{
  width: 28px;
  height: 32px;
  padding: 0 12px;
  margin-bottom: 12px;
  margin-right: 8.004px;
  background-color: rgb(242,243,245);
  align-items: center;
  color: rgb(81,87,103);
  display: flex;
  border-radius: 4px;
  font-size: 14.004px;
  line-height: 32.0131px;
  float: left;

}
.tab_title{
  width: 42px;
  height: 44px;
  margin-right: 8px;
  color: rgb(81,87,103);
  font-family: -apple-system, system-ui, "Segoe UI", Roboto, Ubuntu, Cantarell, "Noto Sans", sans-serif, BlinkMacSystemFont, "Helvetica Neue", "PingFang SC", "Hiragino Sans GB", "Microsoft YaHei", Arial
;
  font-size: 14px;
  line-height: 32.004px;
  float: left;

}

.biaoqian{
  display: flex;
  width: 28px;
  height: 32px;
  padding: 0 12px;
  margin-bottom: 12px;
  margin-right: 8.004px;
  align-items: center;
  background-color: rgb(234,242,255);
  border-radius: 4px;
  color:rgb(30,128,255);
  font-family: -apple-system, system-ui, "Segoe UI", Roboto, Ubuntu, Cantarell, "Noto Sans", sans-serif, BlinkMacSystemFont, "Helvetica Neue", "PingFang SC", "Hiragino Sans GB", "Microsoft YaHei", Arial
;
  font-size: 14.004px;
  line-height: 32.0131px;
  float: left;
}


.markdown{
  background-image: linear-gradient(90deg,rgba(50,0,0,.05) 3%,transparent 0),linear-gradient(1turn,rgba(50,0,0,.05) 3%,transparent 0);;
  /* background-position-x: 50%,50%;
  background-position-y: 50%,50%; */
  background-position: 50%;
  background-size: 20px 20px;


}

.catelog_title{
  width: 260px;
  height: 24px;
  padding: 15.996px 0;
  margin: 0 20.004px;
  border-bottom: 1px rgb(228,230,235) solid;
  color: rgb(29,33,41);
  font-size: 16px;
  font-weight: 500;
  line-height: 24px;
  background-color: white;
  float: right;
  margin-bottom: 8px;
    }

</style>