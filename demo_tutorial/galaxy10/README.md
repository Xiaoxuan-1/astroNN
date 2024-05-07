该项目难点主要在于深度学习环境的配置，详情参见博客【2024年04月24日基于Galaxy10CNN的星系形态分类项目实战，TensorFlow环境配置踩坑及记录】：http://t.csdnimg.cn/wwzoS

具体如下：Tensorflow==2.12.1

该版本仍会有两个报错，也是版本不完全匹配导致的，但是该版本不匹配可以将报错的代码注释掉，即可顺利跑通。

第一个报错：`sample_weight_mode = sample_weight_mode`注释掉这句即可

![在这里插入图片描述](https://img-blog.csdnimg.cn/direct/8af0389f336d4f37898d47364d13fd30.png)

第二个报错：报错TensorFlow版本小于2.13，请升级版本！注意，此时千万不要升级版本，把报错的地方，即需要使用2.13版本TensorFlow的代码注释掉即可，只要不影响功能的实现即可。

![在这里插入图片描述](https://img-blog.csdnimg.cn/direct/8e2dd489d48148d79f45383654ffbabc.png)

该文件中注释掉的部分即为使用2.13版本的TensorFlow，注释掉即可（可能2.13版本的可以跳过这个错误直接实现，但笔者没有尝试）：

![在这里插入图片描述](https://img-blog.csdnimg.cn/direct/87dbbb0bab05413794fb31beb9451b07.png)

到此为此，程序即可跑通，进入训练即可，可自行修改训练参数。
