# Gait-Recognition-via-View-Aware-Part-Wise-Attention-and-Multi-Scale-Dilated-Temporal-Extractor
#### 使用说明

1.  下载 [CASIA-B Dataset](http://www.cbsr.ia.ac.cn/english/Gait%20Databases.asp)和[OU-MVLP Dataset](http://www.am.sanken.osakau.ac.jp/BiometricDB/GaitMVLP.html)，参考[GaitSet](https://github.com/AbnerHqC/GaitSet)预处理方式将轮廓裁剪为**64x64**大小
2.  配置虚拟环境
- Python 3.6
- PyTorch 1.3.1
3. 运行程序

Train a model by
```bash
python train.py
```
- `--cache` if set as TRUE all the training data will be loaded at once before the training start.
This will accelerate the training.
**Note that** if this arg is set as FALSE, samples will NOT be kept in the memory
even they have been used in the former iterations. #Default: TRUE

Evaluate the trained model by
```bash
python test.py
```
- `--iter` iteration of the checkpoint to load. #Default: 20000
- `--batch_size` batch size of the parallel test. #Default: 1
- `--cache` if set as TRUE all the test data will be loaded at once before the transforming start.
This might accelerate the testing. #Default: FALSE

#### Citation
- Gait Recognition via View-Aware Part-Wise Attention and Multi-Scale Dilated Temporal Extractor
