# 0001 poetry
  
  poetry����rnn���ɹ�ʫ��demo����Ϊֻѵ����100��epoch��ѵ���ٶȽϿ졣
  
  ���Ի�����win10 python3.6.1 tensorflow1.2.1
  
  data/poetry.txt��ѵ�����ݣ�ʫ���ı���
  
  model Ŀ¼�������Ѿ�ѵ���õ�ģ�͡�
  
  train_poetry_model.py����ѵ��ģ�ͣ����Ҫ�Լ�ѵ��������ɾ��modelĿ¼�������ʵ����� epoch ��ֵ��
  
  test_poetry.py �������һ��ʫ��
  
  test_acrostic_poetry.py ����һ�ײ�ͷʫ���޸� print(gen_head_poetry(u'�ﾺ����', 7)) �еĲ������������ͬ��ͷʫ��


# 0002 SpecificFaceRecognition
  ʹ��tensorflow dlib opencv�ض�����ʶ��
  ```
  pip3 install tensorflow==1.2.1
  pip3 install tensorflow_gpu==1.2.1
  pip3 install numpy==1.13.1+mkl
  pip3 install opencv-python==3.2.0
  pip3 install dlib==19.4.0
  # һ��Ҫע��scikit-learn��scipy�İ汾
  pip3 install scikit-learn==0.18.2
  pip3 install scipy==0.19.1
  ```
  ```
  # ��blog�����ο� http://tumumu.cn/2017/05/02/deep-learning-face/
  # Դ���ַ:https://github.com/5455945/tensorflow_demo.git
  # win10 Tensorflow_gpu1.2.1 python3.5.3 dlib opencv
  # CUDA v8.0 cudnn-8.0-windows10-x64-v5.1
  # ��ʵ����Ҫ��һ������ͷ���ʼǱ��Դ��ļ���
  # tensorflow_demo\SpecificFaceRecognition\get_my_faces.py ��dlib�����Լ�����jpgͼ��
  # tensorflow_demo\SpecificFaceRecognition\get_my_faces_opencv.py ��opencv�����Լ�����jpgͼ��(Ч��û��dlib��)
  # tensorflow_demo\SpecificFaceRecognition\set_other_faces.py Ԥ����lfw����������
  # tensorflow_demo\SpecificFaceRecognition\train_faces.py ����ʶ��ѵ��
  # tensorflow_demo\SpecificFaceRecognition\is_my_face.py ����ʶ�����
  ```
  
  *01 ��ȡ����ͼƬ��*
  ʹ��`get_my_faces.py`��ȡ���˵�10000��ͷ����Ƭ�����浽`./my_faces`Ŀ¼��ֻ������`get_my_faces.py`�����ڵ���ǰ���ڳ���ͬ������������Ƽ��ɡ���Լ1Сʱ���ҿɲɼ�10000�š�
  `get_my_faces_opencv.py`�ǲ���opencv��ɼ��ģ��ٶȱ�dlib��`get_my_faces.py`��Щ��dlibЧ�����Щ��

  *02 ��ȡ��������ͼƬ��*
  ���� http://vis-www.cs.umass.edu/lfw/lfw.tgz �������ݼ���
  windows�£�����ʹ��winrar��ѹ��ע��Ҫ��ѡ[�鿴�ļ�]��Ȼ���ٽ�ѹ�����ܽ�ѹ��������Ŀ¼���ļ���
  ��ѹ����ļ��ŵ�`./input_img`Ŀ¼�¡�
  Ȼ��ʹ��`set_other_people.py`����`./input_img`Ŀ¼�µĽ�ѹ�ļ����Ѵ�Լ13000+��ͷ��Ԥ����`./other_faces`Ŀ¼��
  
  *03 ѵ��ģ��*
  ʹ��`train_faces.py`��ѵ��ģ�ͣ�ģ�ͱ��ֵ�`./model`Ŀ¼��

  *04ʹ��ģ�ͽ���ʶ��*
  ʹ��`is_my_face.py`����֤ģ�ͣ���⵽���Լ�����ʱ������true��

