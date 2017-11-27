# Layout布局
写sass也有一段时间了，在初始化布局及组件化的css方面有了一点自己的想法和方法，于是写下，供以后自己或他人使用。
## 包含文件  
### 统一入口  
- layout.scss
### 应包含文件  
> 网格系统
- bootstrap.scss  
> 混合指令
- mixin.scss
> 统一字体及字体图标配置
- font.scss  
  
## 详细使用说明
### layout
- 负责整体body的布局
- 承当唯一入口
- 负责自定义保留字样式的存放  

初始化：  
1.删除```<i>```标签默认斜体  
2.设置```<a>```标签hover、active、focus、visited的```text-decoration```属性为**none**  


保留字详细：  
| 名称 | 方法 | 
| - | :-: |
| .clearfix | 清除float浮动 |
| .hidden | ```display:none``` |
| .text-left| ```text-align:left``` |
| .text-right| ```text-align:right``` |
| .text-center| ```text-align:center```|
| .text-yellow| ```color:#fbd319``` |
| .text-red | ```color:#dc1c24``` |
| .text-gray| ```color:#808080``` |
| .list-unstyled | ```list-style:none;margin:0;padding-left:0``` |
### bootstrap
- 负责网格系统
- 优化默认的Table、Forms、Buttons标签
- 该样式可以[定制化](http://v3.bootcss.com/customize/)
- 保留字请[点击这里查看](http://v3.bootcss.com/css/#grid)

### mixin
- 负责混合指令及方法的存放

方法：  
| 方法 | 用法 | 参数 |  
| - | :-: | -: |
| m-auto() |设置元素```margin```值 | ```$top:0,```<br>```$bottom:0,```<br>```$leftRight:0``` |
| solid() | 设置边框，可设置全边框也可设置单边框,```$p```为0时为全边框，为left、right、top、bottom时对应相应边框| ```$px:1px,```<br>```$color:#808080,```<br>```$p:0,```<br>```$s:solid```|
| bg() | 设置背景图，一般先定义一个共用文件夹路径，调用url时可直接```$url:'{$path}image.jpg'```| $url:null<br>$size:cover<br>$position:50% 50%|
| flex() | 设置flex布局，默认alig-item、justify-content为center | $align-item:center,<br> $justify-content:center |
| border-radius() | 为保证border-radius的兼容性 | $radius |
| transform() | 设置过渡动画，保证兼容性 | $transform |
| user-select() | 设置文字选择，默认不可选 | $param:none |
| box-shadow() | 设置盒子阴影，默认无 | $param:none |


### font
- 负责字体库的存放
- 负责页面默认字体的设置
- 负责字体图标及保留字的存放