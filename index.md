<ul class="main_content" style="padding-left: 0;">
  <li><p class="date">January 13, 2019</p><h4 class="title"><a href="study/rm/?content=judgement">裁判系统数据读取探索</a></h4><div class="excerpt"><p>RM备赛期间遇到需要读取裁判系统的数据，在此将学习过程记录下来。因为RM2019的裁判系统的通信协议还没有出来，所以我学习的是RM2018版的裁判系统的数据获取。</p><p>USART配置</p><p>我这里选用的是USART2，采用异步通信模式，并使能DMA，同时打开串口全局中断和DMA中断，波特率115200，数据位8位，停止位1位，无奇偶校验位。</p></div><ul class="meta"><li>big_uncle</li><li><a href="study/rm/">RM比赛</a></li></ul></li>
  <li><p class="date">January 11, 2019</p><h4 class="title"><a href="study/rm/?content=int_to_short">关于电机数据为无符号整形的处理</a></h4><div class="excerpt"><p>前段时间我使用电机的时候，在电机的数据结构体中都是使用int类型。</p>```c
struct CAN_Motor
{
    int fdbPosition;        //电机的编码器反馈值
    int last_fdbPosition;   //电机上次的编码器反馈值
    int bias_position;      //机器人初始状态电机位置环设定值
    int fdbSpeed;           //电机反馈的转速/rpm
    int round;              //电机转过的圈数
    int real_position;      //过零处理后的电机转子位置
};
```</div><ul class="meta"><li>big_uncle</li><li><a href="study/rm/">RM比赛</a></li></ul></li>
  <li><p class="date">January 11, 2019</p><h4 class="title"><a href="study/rm/?content=jtag_swd">JTAG与SWD接线口转换</a></h4><div class="excerpt"><p>开发STM32时常在20pin的JTAG接口和4pin的SWD接口之间转换，但时间一长就记不住它们的线序对应关系，每次都去百度找感觉很麻烦，这次直接把它录进来。</p></div><ul class="meta"><li>big_uncle</li><li><a href="study/rm/">RM比赛</a></li></ul></li>
  <li><p class="date">January 10, 2019</p><h4 class="title"><a href="study/web/?content=phaser_2">Phaser 飞机大战学习（二）</a></h4><div class="excerpt"><p>Phaser 飞机大战学习-第二课</p><p>图片加载</p><p>背景图片科技使用`game.add.image(0,0,'backgroud')`，也可以使用`game.add.sprite(0,0,'background')`。</p></div><ul class="meta"><li>big_uncle</li><li><a href="study/web/">Web学习</a></li></ul></li>
  <li><p class="date">January 10, 2019</p><h4 class="title"><a href="study/web/?content=phaser_1">Phaser 飞机大战学习（一）</a></h4><div class="excerpt"><p>Phaser 飞机大战学习-第一课</p><p>从前年开始我就一直想进军H5游戏的领域，但是当时知识尚欠，连CANVAS这个标签都学不下去，后来我接触到了[three.js](https://github.com/mrdoob/three.js)和[pixi.js](https://github.com/pixijs/pixi.js)，一个是3D的，基于WebGL，一个是2D的，都很厉害，但最后都因为各种原因没有学下去。</p><p>前段时间我接触无意间接触到了phaser.js，这个游戏框架是专门用于2D游戏开发的，其实不只是开发游戏，动画也是可以做的。phaser.js框架好处在于它的小巧，而且是基于pixi.js的，入手很方便，但目前它的中文资料还不是很多，中文资料里面最赞的是[phaser小站](https://www.phaser-china.com/)，我的phaser学习也是通过这个小站入门的，这里就记录一下我前段时间学习phaser的一些收获</p></div><ul class="meta"><li>big_uncle</li><li><a href="study/web/">Web学习</a></li></ul></li>
  <li><p class="date">January 9, 2019</p><h4 class="title"><a href="study/college/?content=meterials_forming">材料成形基本原理复习</a></h4><div class="excerpt"><p>材料成形基本原理-复习</p><p>大三上</p></div><ul class="meta"><li>big_uncle</li><li><a href="study/college/">大学学习</a></li></ul></li>
  <li><p class="date">January 8, 2019</p><h4 class="title"><a href="study/rm/?content=infantry_chassis">步兵车底盘驱动</a></h4><div class="excerpt"><p>底盘作为一个机器人最基础的东西，是各位必须掌握的。但是看着大家的任务完成进度感到焦心，所以写了这篇步兵车底盘驱动代码的详解，以及底盘调试的步骤和要点。</p><p>工程简介</p><p>这篇教程里的代码使用STM32F405RGT6芯片，使用STM32CubeMX软件辅助进行开发。</p></div><ul class="meta"><li>big_uncle</li><li><a href="study/rm/">RM比赛</a></li></ul></li>
  <li><p class="date">January 8, 2019</p><h4 class="title"><a href="study/rm/?content=basic_knowladge">电控基础知识点</a></h4><div class="excerpt"><p>写在最前</p><p>本网页将我这一年（2018年）的电控经历积累下来的知识和经验，以及下半年进行的两次培训的内容和要点做了一个综合总结。</p><p>上半年我一直用的是标准库进行编程，但自从国庆期间用上**HAL库**之后，我被HAL库的便捷深深打动，自此基本放弃了标准库，所以本总结的内容是基于HAL库的，并结合**STM32CubeMX**软件*（因为过程有些繁琐，截图很麻烦，所以本总结并不会贴出STM32CubeMX上的相关配置过程）*。</p></div><ul class="meta"><li>big_uncle</li><li><a href="study/rm/">RM比赛</a></li></ul></li>
  <li><p class="date">January 8, 2019</p><h4 class="title"><a href="study/web/?content=create_blog">博客搭建过程</a></h4><div class="excerpt"><p>最近正值期末考试，今天刚考完一门，昨晚上实在是不想复习了，正想着怎么办的时候，突然想把复习的考点放在自己的博客上，正好我半年前搭建了一个博客，打开一看发现只有最开始搭建的时候的一篇博客，感觉很失败。</p><p>之前的这篇博客采用的是Hexo+NexT框架搭建的，但是我的电脑几经改装，系统也重装了几次，node.js早就没了，想要继续维护这个博客有些麻烦，索性全删了，从头手写一个博客。</p></div><ul class="meta"><li>big_uncle</li><li><a href="study/web/">Web学习</a></li></ul></li>
  <li><p class="date">January 7, 2019</p><h4 class="title"><a href="study/college/?content=semiconductor">半导体物理复习</a></h4><div class="excerpt"><p>半导体物理与器件-复习</p><p>大三上</p></div><ul class="meta"><li>big_uncle</li><li><a href="study/college/">大学学习</a></li></ul></li>
</ul>