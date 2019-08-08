# __测试环境：win10-64位和win7-64位__
（系统必须是64位，因为TensorFlow目前只支持64位）
# 一、安装Anaconda3
## 1.下载Anaconda3
Anaconda官网链接:[link](https://www.anaconda.com/download/)
这里我们选择Windows版本，python3.6-version-64位，如下图所示。
![Anaconda3下载界面](https://img-blog.csdn.net/20181013095543580?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0RvY3RvckN1aUxhYg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
## 2.下载完成之后，点击安装Anaconda3
![Anaconda3安装界面](https://img-blog.csdn.net/20181013095811356?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0RvY3RvckN1aUxhYg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
![选择用户](https://img-blog.csdn.net/20181013095843316?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0RvY3RvckN1aUxhYg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
_注意：安装过程中要选择添加环境变量，如下图_
![添加环境变量](https://img-blog.csdn.net/2018101309595995?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0RvY3RvckN1aUxhYg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
待安装完成之后，在开始菜单可以看到Anaconda3（64-bit），如下图所示，其中包括Jupyter Notebook、spyder等。
![安装完成](https://img-blog.csdn.net/20181013100143940?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0RvY3RvckN1aUxhYg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

# 二、TensorFlow安装教程

## 1.TensorFlow安装
1.1 打开刚才下好的Anaconda Prompt，建立一个python3.6的conda计算环境，命名为tensorflow。在终端中输入：
```python
conda create -n tensorflow python=3.6
```
1.2 用命令激活这个环境：
```python
activate tensorflow
```
1.3 激活后会在路径前面出现“（tensorflow）”，如下图所示。
![激活的tensorflow环境](https://img-blog.csdn.net/20181013102026254?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0RvY3RvckN1aUxhYg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
1.4 tensorflow-CPU版本，用pip安装tensorflow，输入以下命令：
```python
pip install tensorflow 
```
tensorflow-GPU版本（需要安装CUDA及CUDNN），用pip安装tensorflow，输入以下命令：
（_注意：有时因为网速等原因，会安装失败，可以多试几次安装命令_）。
```python
pip install tensorflow-gpu  
```
1.5 测试是否安装成功，在终端进入python，并运行一个简单的例子：
```python
python
import tensorflow as tf
hello = tf.constant("hello, tensorflow! ")
sess = tf.Session()
print(sess.run(hello)) 
```
```
# 输出结果
b'hello, tensorflow!'
```
1.6 每次打开终端，使用TensorFlow的时候都需要激活conda环境，即在cmd中先输入：
```python
activate tensorflow
```
退出TensorFlow环境，输入命令：
```python
deactivate
```
1.7．查看环境信息：
```python
conda info --envs
```
## 2.更新tensorflow的版本
2.1.查看tensorflow版本（在python中输入，注意version前后都有两个下划线）：
```python
print(tf.__version__)
```
2.2.更新tensorflow的版本
在Anaconda Prompt中输入如下命令：
```python
#更新的时候网络可能不好，有时需要多尝试几次才能成功
activate tensoflow
pip install --upgrade tensorflow
```
在anaconda里更新tensorflow到指定版本：
```python
activate tensoflow
pip install -U  tensorflow==1.4
```
2.3.更新TensorFlow中的python版本，如：python3.6，在终端中输入：
```python
activate tensorflow
conda install python=3.6
```
## 3.使用Anaconda Navigator管理python环境
打开Anaconda Navigator
![Anaconda Navigator](https://img-blog.csdn.net/20181013110218701?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0RvY3RvckN1aUxhYg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
选择新建的tensorflow环境，安装带有tensorflow环境的jupyter和spyder等软件。
![选择新建的tensorflow环境，安装jupyter和spyder](https://img-blog.csdn.net/20181013110551420?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0RvY3RvckN1aUxhYg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
最后，推荐吴恩达免费的深度学习网络课程:[link](https://mooc.study.163.com/smartSpec/detail/1001319001.htm)，以及课后编程作业。
