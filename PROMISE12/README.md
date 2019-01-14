在Promise12上做尝试

首先尝试了不用aug,直接1257个图片去网络里train,最后一层也没有flatten而是直接sigmoid,val loss 
- 0.28
- AEP 0.557,明显要好

修正了loss 最后一层用softmax,
- 0.7302
- AEP 0.75676


加上flo rflo:
- 两个都不用, 自己的网络结构:0.751
- 加到最后一层:0.771/0.776左右,用log或者clip差不多
- 用Unet+dropout: 0.75
- Unet+dropout+flo+rflo: 0.823
- Unet+dropout+flo+rflo+last layer conv = 0.8425
- Unet+dropout再跑一次:0.83
这几个差不多..

然后加上了data-augmentation,出来的AUGnet 训练非常缓慢...


- Dilation Does Work. especially with 2222
- Without Dilation, Flo can make attributes to seg
