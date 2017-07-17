# 0001 poetry
  
  poetry是用rnn生成古诗的demo。因为只训练了100个epoch，训练速度较快。
  
  测试环境：win10 python3.6.1 tensorflow1.2.1
  
  data/poetry.txt是训练数据，诗词文本。
  
  model 目录下面有已经训练好的模型。
  
  train_poetry_model.py用来训练模型，如果要自己训练，可以删除model目录，并且适当调整 epoch 的值。
  
  test_poetry.py 随机生成一首诗。
  
  test_acrostic_poetry.py 生成一首藏头诗。修改 print(gen_head_poetry(u'物竞天择', 7)) 中的参数，会输出不同藏头诗。
