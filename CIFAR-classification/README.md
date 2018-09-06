test on cifar-10 classification dataset

res18 5513结构,没有downsample,
- AEP:0.83,0.74
- res:0.85,0.76
结论是没什么用

如果结构是5533,结果变差了,不知道为啥...凉凉

在此基础上尝试小样本:
- res: 0.5886
- AEP: 0.5178

res18 5d51u3结构
- AEP: running,0906 : 0.6044(not aug 50k)
- res: 0.76(no aug )

55133:
- AEP: 5k 


