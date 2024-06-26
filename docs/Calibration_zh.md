# 校准

> iSpindle 漂浮在麦汁当中的倾斜角度可以转换成柏拉图度（ºPlato）、比重值（SG）或者其他单位。为了能够做到这一点，应该在 iSpindle 的倾斜度与所选择单位之间建立起参照.。必须对参考值进行测量，并使用 Excel 表格制作图表以及生成公式。 Excel 会计算 iSpindle 的倾斜角度与柏拉图度、比重值或其他单位之间的关系。 由于每个自己做的 iSpindle 会有所不同，因此需要对单独每个 iSpindle 进行参考测量，但只需要进行一次。

***

# 目录
- [简易方法 (I)](#easy-method-(I))
- [改进方法利用快速发酵 (II)](#improved-method-using-fast-fermenting-(II))
- [ Excel 图表公式](#formula)

***

## 简易方法 (I)

建议您将 iSpindel 与 [Ubidots](https://ubidots.com/) 连接，方便读取测量的倾斜角度。此外，明智的做法是更改 iSpindel 中的设置，以便每 20 秒发送一次新的读数。在如此短的时间间隔内，可以在 [Ubidots](https://ubidots.com/) 网站上轻松地跟踪测量结果。

1. 将 iSpindel 放入干净的清水中 (柏拉图 0 度，比重值 1.000) 
> ***记下 iSpindel 的倾斜角度***

2. 制作达到最大预期密度的糖水溶液。如果你要酿造初始比重较高的烈性啤酒，你应该在这个高比重范围内的预期参考测量值。对于大多数酿酒师来说，比重在 1.085 左右或 柏拉图 20 度 左右的目标密度溶液就够了。   
> *糖溶液示例: 400 毫升 和 100 克糖*     
> ***测量比重值或者柏拉图度并和 iSpindel 倾斜角度一起记下来***

3. 用水稀释上述溶液，直到它达到 柏拉图 15 度 或者 比重 1.061       
>*示例：用 166 毫升水稀释第 2 点的溶液*     
>***测量比重值或者柏拉图度并和 iSpindel 倾斜角度一起记下来***        

4. 从上一点稀释溶液，直到达到约 柏拉图 10 度 或者 比重 1.040       
>*示例：用 333 毫升水稀释第 3 点的溶液*        
>***测量比重值或者柏拉图度并和 iSpindel 倾斜角度一起记下来***     

5. 从上一点稀释溶液，直到达到约 柏拉图 7.5 度 或者 比重 1.030
>*示例：用 333 毫升水稀释第 4 点的溶液*        
>***测量比重值或者柏拉图度并和 iSpindel 倾斜角度一起记下来***     

6. 从上一点稀释溶液，直到达到约 柏拉图 5 度 或者 比重 1.020
>*示例：用 666 毫升水稀释第 5 点的溶液*        
>***测量比重值或者柏拉图度并和 iSpindel 倾斜角度一起记下来***   

7. 从上一点稀释溶液，直到达到约 柏拉图 2.5 度 或者 比重 1.010     
>*示例：用 2000 毫升水稀释第 6 点的溶液*      
>***测量比重值或者柏拉图度并和 iSpindel 的倾斜角度一起记下来        
>在 Excel 表格中输入测量点（见下文），此 Excel 表格将计算出参考公式***

***
 
## 改进方法利用快速发酵 (II)

这种方法更为精确，因为它会考虑到发酵过程中产生的二氧化碳对 iSpindel 造成的影响。

建议您将 iSpindel 与 [Ubidots](https://ubidots.com/) 连接，方便读取测量的倾斜角度。此外，明智的做法是更改 iSpindel 中的设置，以便每 20 秒发送一次新的读数。在如此短的时间间隔内，可以在 [Ubidots](https://ubidots.com/) 网站上轻松地跟踪测量结果。

1. 将 iSpindel 放入干净的（自来）水中 (柏拉图 0 度，比重值 1.000)       
>***记下 iSpindel 测量的倾斜角度***

2. 制作达到最大预期密度的糖水溶液。如果你要酿造初始比重较高的烈性啤酒，你应该在这个高比重范围内的预期参考测量值。对于大多数酿酒师来说，比重在 1.085 左右或 柏拉图 20 度 左右的目标密度溶液就够了。  
>*糖溶液示例: 800 毫升 水 + 200 克 冰糖*

3. 加入酵母到糖溶液，让 iSpindel 在溶液中漂浮         
>***测量比重值或者柏拉图度并和 iSpindel 倾斜角度一起记下来***

4. 每隔一段时间测量液体的比重值以及 iSpindle 相应的倾斜角度，直至发酵结束。      
>***在 Excel 表格中输入记录下来的测量值，得出校准曲线公式***     
>
>***注意：如果使用折光仪来测量白利糖度，则必须重新计算得到的测量值，加上酒精度数以进行校正*** 

***

# 公式

- ## [在线比重校准工具](http://www.ispindel.de/tools/calibration/calibration.htm)

可以在不同的选项 比重/柏拉图或者白利糖度 中输入相对应的测量值以及倾斜角度。它将计算出第二回和第三回的角度公式，获取倾斜角度的读数就可以预测出比重值或柏拉图度。必须在固件中输入角度公式才能得到比重值或柏拉图度的数值。

***

- ## Excel 表格

获取的测量值可以输入到Excel表格中,该表格将计算出一个公式来预测给定倾斜值的比重值或柏拉图度。这个公式必须输进固件配置中，以便能够获取比重值或柏拉图度的读数。
其它读数例如表观衰减度或者酒精百分比，可以通过使用 [Ubidots](https://ubidots.com/) 中的 'Derived Variable'（衍生变量)以类似的方式获得。

1. 首先在 Excel 中输入测量值：
[下载 Excel 表格](https://github.com/universam1/iSpindel/blob/master/docs/Kalibrierung_zh.xlsm)
2. 通过点击按钮启动宏 **公式更新** ，接着公式将会被更新。 
![Excelcalc](/pics/Excelcalc.jpg)
3. 在 [Ubidots](https://ubidots.com/) 账号中必须添加 **Derived Variable** （衍生变量）。这是一个以其他变量为来源进行计算的变量，这可以通过执行接下来的步骤来完成。
4. 在 [Ubidots](https://ubidots.com/) 中转到 **Source** 这一项
5. 选择 iSpindel 为来源
6. 点击 **(+) 添加变量** 
7. 选择 **Derived** 这一项      
![Derived](/pics/Ubiderived.jpg)
1. 现在你可以将 Excel 中的公式填写进去。公式中 ***(tilt)*** 的部分必须被替换掉。为此请单击 ***insert variable*** 然后选取 **tilt**，给新创建的变量一个有意义的名字，比如比重或柏拉图。    
![Ubiplato](/pics/Ubiplato.jpg)
9. 在 **Dashboard** 你可以创建测量数据的图形演示。
