# 下载Opencv源码

https://github.com/opencv/opencv（opencv）

https://github.com/opencv/opencv_contrib（opencv-contrib）



# 安装cmake工具

https://cmake.org/

[CSDN安装教程](https://blog.csdn.net/qq_42598221/article/details/121952160?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522165559276316782246424935%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=165559276316782246424935&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-1-121952160-null-null.142^v17^pc_rank_34,157^v15^new_3&utm_term=cmake%E5%AE%89%E8%A3%85&spm=1018.2226.3001.4187)



# 编译过程

![img](file:///C:\Users\98503\AppData\Roaming\Tencent\Users\985031259\QQ\WinTemp\RichOle\1`ELTW$K[%XP`~~G%@GBP$Q.png)

编译后的文件夹的存放地址最好在被编译的文件后面新建一个

关于OPencv源码我勾选了

- OPENCV_ENABLE_NONFREE
- OPENCV_EXTRA_MODULES_PATH（这里地址选择opencv-contrib模块的源码）

- BUILD_opencv_world
- 如果出现ade有报错可以取消勾选WITH_ADE
- **NOT SUPPORTED: validate setupvars script in install directory**如果报这个错误，只需去除 OPENCV_GENERATE_SETUPVARS选项

然后configure没有报错之后点击generate

**configure没有报错是指没有出现红色的字体提醒**

如果有在cmake后的文件夹里面找到 **CMakeDownloadLog.txt**这个文件，然后根据文件提示的内容去**手动下载**里面的文件。

用校园网configure可能会有奇效。

[参考文件](https://www.cnblogs.com/huluwa508/p/10142718.html)



# 打开Opencv工程

打开后对其中的 **INSTALL和ALL_BUILD**进行生成

先对INSTALL生成，然后把报语法错误的地方后面的三句日语注释删除，再次生成。

如果还有报文件缺失的错误，或者头文件打不开找不到之类的。则根据不同去网上找解决办法，手动下载文件。

如果有报 **pythonxx_d.lib**

[解决办法1](https://blog.csdn.net/weixin_43788499/article/details/84933210?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522165559451716782395310830%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=165559451716782395310830&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~baidu_landing_v2~default-2-84933210-null-null.142^v17^pc_rank_34,157^v15^new_3&utm_term=%E6%97%A0%E6%B3%95%E6%89%93%E5%BC%80+python37_d.lib+&spm=1018.2226.3001.4187)

去设置->应用->应用和功能

搜索python，点击修改，添加上debug就可以



解决办法2：
去python[官网](https://www.python.org/downloads/source/)下载对应版本的python安装程序，然后把**pythonxx_d.lib**文件复制到原来python的目录下即可（该方法适用python在anconada中下载的用户）

# 完成

把生成不报错的源码按常规链接到我们需要的工程中就行。源码的东西都在install文件下。



再附上两个视频教程

[b站](https://www.bilibili.com/video/BV1Qq4y1Y7vc?spm_id_from=333.1007.top_right_bar_window_custom_collection.content.click&vd_source=483d14e068af3ba58eedbb77813e539d)

[youtobe](https://www.youtube.com/watch?v=m9HBM1m_EMU&list=PLkmvobsnE0GHMmTF7GTzJnCISue1L9fJn&index=28)