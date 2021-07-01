# Smoke_Fire_Detection
火灾场景的烟雾-火焰检测

## 介绍

本模型基于yolov5框架，并对yolov5中neck-PANet部分作出了改进

weights中smoke_fire.pt是最终选择的模型，因为文件过大放不上github，选择上传百度云，
链接：https://pan.baidu.com/s/1jJv3Y6wC9LJdahAzDTJcBg 
提取码：gyd5 

运行时更改图片路径后直接运行detect.py即可，放入图片、含图片文件夹、视频皆可，仅需改变‘--source’的内容，操作如下：

①默认为图片/视频模式：
图片/视频默认路径为test/image 文件夹，一次检测文件夹中所有图片/视频
运行时默认不显示结果图片，运行后的结果保存在runs/detect/exp1,2,... 文件夹中（exp后面的数字表示第几次的运行结果）

若要在运行时显示，请在182行(view-img)加入default=True

②实时模式
176行  default='test/images'  改成  default='0'  
停止实时观看并保存视频，请按'q'
（注意，若要修改对应参数，请在174行往后改）

train、test所需数据集data0已上传百度云，链接：https://pan.baidu.com/s/1gaOFeHdqwmYAqQVbIMqnVw 
提取码：z708 

其中1660张为网上数据集中自己label修订后得到（发现网上数据集存在label标注误差大、对烟的标注极少的问题），3320张为数据增强后获得。

## 运行后的效果图对比：
![image](https://github.com/sysu19351164/SF_Detection/blob/main/readme-images/001.png)  ![image](https://github.com/sysu19351164/SF_Detection/blob/main/readme-images/001-detect.png)

其余对比图见readme-images
