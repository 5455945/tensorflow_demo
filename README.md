# 0001 poetry
  
  poetry是用rnn生成古诗的demo。因为只训练了100个epoch，训练速度较快。
  
  测试环境：win10 python3.6.1 tensorflow1.2.1
  
  data/poetry.txt是训练数据，诗词文本。
  
  model 目录下面有已经训练好的模型。
  
  train_poetry_model.py用来训练模型，如果要自己训练，可以删除model目录，并且适当调整 epoch 的值。
  
  test_poetry.py 随机生成一首诗。
  
  test_acrostic_poetry.py 生成一首藏头诗。修改 print(gen_head_poetry(u'物竞天择', 7)) 中的参数，会输出不同藏头诗。


# 0002 SpecificFaceRecognition
  使用tensorflow dlib opencv特定人脸识别
  ```
  pip3 install tensorflow==1.2.1
  pip3 install tensorflow_gpu==1.2.1
  pip3 install numpy==1.13.1+mkl
  pip3 install opencv-python==3.2.0
  pip3 install dlib==19.4.0
  # 一定要注意scikit-learn和scipy的版本
  pip3 install scikit-learn==0.18.2
  pip3 install scipy==0.19.1
  ```
  ```
  # 该blog完整参考 http://tumumu.cn/2017/05/02/deep-learning-face/
  # 源码地址:https://github.com/5455945/tensorflow_demo.git
  # win10 Tensorflow_gpu1.2.1 python3.5.3 dlib opencv
  # CUDA v8.0 cudnn-8.0-windows10-x64-v5.1
  # 本实验需要有一个摄像头，笔记本自带的即可
  # tensorflow_demo\SpecificFaceRecognition\get_my_faces.py 用dlib生成自己脸的jpg图像
  # tensorflow_demo\SpecificFaceRecognition\get_my_faces_opencv.py 用opencv生成自己脸的jpg图像(效果没有dlib好)
  # tensorflow_demo\SpecificFaceRecognition\set_other_faces.py 预处理lfw的人脸数据
  # tensorflow_demo\SpecificFaceRecognition\train_faces.py 人脸识别训练
  # tensorflow_demo\SpecificFaceRecognition\is_my_face.py 人脸识别测试
  ```
  
  *01 获取本人图片集*
  使用`get_my_faces.py`获取本人的10000张头像照片，保存到`./my_faces`目录。只需启动`get_my_faces.py`，坐在电脑前，摆出不同脸部表情和姿势即可。大约1小时左右可采集10000张。
  `get_my_faces_opencv.py`是采用opencv库采集的，速度比dlib的`get_my_faces.py`快些。dlib效果会好些。

  *02 获取其他人脸图片集*
  下载 http://vis-www.cs.umass.edu/lfw/lfw.tgz 人脸数据集。
  windows下，可以使用winrar解压，注意要先选[查看文件]，然后再解压，才能解压出所有子目录及文件。
  加压后的文件放到`./input_img`目录下。
  然后，使用`set_other_people.py`处理`./input_img`目录下的解压文件，把大约13000+张头像预处理到`./other_faces`目录。
  
  *03 训练模型*
  使用`train_faces.py`来训练模型，模型保持到`./model`目录下

  *04使用模型进行识别*
  使用`is_my_face.py`来验证模型，检测到是自己的脸时，返回true。

