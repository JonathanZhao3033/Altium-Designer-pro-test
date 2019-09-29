﻿# Altium-Designer-pro-test
AD板层定义介绍

1、顶层信号层(Top Layer)：也称元件层,主要用来放置元器件,对于比层板和多层板可以用来布线；

2、中间信号层(Mid Layer)： 最多可有30层,在多层板中用于布信号线.

3、底层信号层(Bootom Layer)：也称焊接层,主要用于布线及焊接,有时也可放置元器件.

4、顶部丝印层(Top Overlayer)：用于标注元器件的投影轮廓、元器件的标号、标称值或型号及各种注释字符。

5、底部丝印层(Bottom Overlayer)：与顶部丝印层作用相同，如果各种标注在顶部丝印层都含有，那么在底部丝印层就不需要了。

6、内部电源层(Internal Plane)：通常称为内电层，包括供电电源层、参考电源层和地平面信号层。内部电源层为负片形式输出。

7、机械数据层(Mechanical Layer)：定义设计中电路板机械数据的图层。电路板的机械板形定义通过某个机械层设计实现。

8、阻焊层(Solder Mask-焊接面)：有顶部阻焊层(Top solder Mask)和底部阻焊层(Bootom Solder mask)两层，是Protel PCB对应于电路板文件中的焊盘和过孔数据自动生成的板层，主要用于铺设阻焊漆．本板层采用负片输出，所以板层上显示的焊盘和过孔部分代表电路板上不铺阻焊漆的区域，也就是可以进行焊接的部分．

9、锡膏层(Past Mask-面焊面)：有顶部锡膏层(Top Past Mask)和底部锡膏层(Bottom Past mask)两层，它是过焊炉时用来对应ＳＭＤ元件焊点的，也是负片形式输出．板层上显示的焊盘和过孔部分代表电路板上不铺锡膏的区域，也就是不可以进行焊接的部分。

10、禁止布线层(Keep Ou Layer)：定义信号线可以被放置的布线区域，放置信号线进入位定义的功能范围。

11、多层(MultiLayer)：通常与过孔或通孔焊盘设计组合出现，用于描述空洞的层特性。

12、钻孔数据层（Drill）：

solder表示是否阻焊,就是PCB板上是否露铜

paste是开钢网用的,是否开钢网孔

————————————————
版权声明：本文为CSDN博主「先思考后行动」的原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接及本声明。
原文链接是：https://blog.csdn.net/qq_18394821/article/details/48603257


 PCB的各层定义及描述：  

1、  TOP LAYER（顶层布线层）：设计为顶层铜箔走线。如为单面板则没有该层。  


2、  BOMTTOM LAYER（底层布线层）：设计为底层铜箔走线。  


3、  TOP/BOTTOM SOLDER（顶层/底层阻焊绿油层）：顶层/底层敷设阻焊绿油，以防止铜箔上锡，保持绝缘。在焊盘、过孔及本层非电气走线处阻焊绿油开窗。  
l         焊盘在设计中默认会开窗（OVERRIDE：0.1016mm），即焊盘露铜箔，外扩0.1016mm，波峰焊时会上锡。建议不做设计变动，以保证可焊性；  
l         过孔在设计中默认会开窗（OVERRIDE：0.1016mm），即过孔露铜箔，外扩0.1016mm，波峰焊时会上锡。如果设计为防止过孔上锡，不要露铜，则必须将过孔的附加属性SOLDER MASK（阻焊开窗）中的PENTING选项打勾选中，则关闭过孔开窗。  
l         另外本层也可单独进行非电气走线，则阻焊绿油相应开窗。如果是在铜箔走线上面，则用于增强走线过电流能力，焊接时加锡处理；如果是在非铜箔走线上面，一般设计用于做标识和特殊字符丝印，可省掉制作字符丝印层。  


4、  TOP/BOTTOM PASTE（顶层/底层锡膏层）：该层一般用于贴片元件的SMT回流焊过程时上锡膏，和印制板厂家制板没有关系，导出GERBER时可删除，PCB设计时保持默认即可。  


5、  TOP/BOTTOM OVERLAY（顶层/底层丝印层）：设计为各种丝印标识，如元件位号、字符、商标等。  


6、  MECHANICAL LAYERS（机械层）：设计为PCB机械外形，默认LAYER1为外形层。其它LAYER2/3/4等可作为机械尺寸标注或者特殊用途，如某些板子需要制作导电碳油时可以使用LAYER2/3/4等，但是必须在同层标识清楚该层的用途。  


7、  KEEPOUT LAYER（禁止布线层）：设计为禁止布线层，很多设计师也使用做PCB机械外形，如果PCB上同时有KEEPOUT和MECHANICAL LAYER1，则主要看这两层的外形完整度，一般以MECHANICAL LAYER1为准。建议设计时尽量使用MECHANICAL LAYER1作为外形层，如果使用KEEPOUT LAYER作为外形，则不要再使用MECHANICAL LAYER1，避免混淆！  


8、  MIDLAYERS（中间信号层）：多用于多层板，我司设计很少使用。也可作为特殊用途层，但是必须在同层标识清楚该层的用途。  


9、  INTERNAL PLANES（内电层）：用于多层板，我司设计没有使用。  10、MULTI LAYER（通孔层）：通孔焊盘层。  


11、DRILL GUIDE（钻孔定位层）：焊盘及过孔的钻孔的中心定位坐标层。  12、DRILL DRAWING（钻孔描述层）：焊盘及过孔的钻孔孔径尺寸描述层。
有 0 
