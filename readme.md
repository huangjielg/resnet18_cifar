resnet18 cifar10/100 上做的一些测试

# resnet18-pretrain  
  修改 IMG_SIZE=32,64,...224 的值可以用各种大小进行训练。  
  预训练收敛特别快,只需要几个迭代就可以达到90%以上正确率。224时，可以到95%.  


# resnet18-pretrain_cifar100  
  
  实验了yolor中的概念,feature alignment. 也没有达到预期效果。    


  Resnet 18 有 4层。对于某一层的输出,当中图像的一个feature.
  首先正向计算 feature。
  然后逆向计算出一个feature。

  计算feature的偏差的平均值，用来纠正模型的输出。可是测试的结果发现对正确率没有影响。  

  逆向计算feature的方法类似于deepdream。
  