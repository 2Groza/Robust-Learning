在Promise12上做尝试

首先尝试了不用aug,直接1257个图片去网络里train,最后一层也没有flatten而是直接sigmoid,val loss 
- 0.28
- AEP 0.557,明显要好

修正了loss 最后一层用softmax,
- 0.7302
- AEP 0.75676
