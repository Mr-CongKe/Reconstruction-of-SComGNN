# Reconstruction-of-SComGNN
本项目为对于推荐系统模型SComGNN的复现，参考论文《Spectral-Based Graph Neural Networks for Complementary Item Recommendation》以及论文作者提供的开源代码https://github.com/luohaitong/SComGNN

复现实验用于完成《机器学习》课程的期末大作业，在此特此对论文作者致谢，感谢！

以下为实验代码运行的一些基本步骤：
-数据预处理

1.需要在https://nijianmo.github.io/amazon/index.html.中下载真实电子商务的数据作为实验数据集

2.将下载的数据集放到./data_preprocess/raw_data/目录下

3.将数据集的文件名改为meta_{}的形式，如meta_Appliances

4.将run.sh的dataset设置为meta_{}中{}的内容，如若数据集文件名为meta_Appliances，则令dataset=Appliances

5.通过以下命令对数据集进行预处理：
 		```
    cd data_preprocess
    sh run.sh
    ```
    
-实验运行

1.在Appliances数据集上训练SComGNN示例：
```
python run.py
```
2.在Toys数据集上训练SComGNN (w/o a)示例:
```
python run.py --dataset Toys --lr 0.01 --mode concat
```
3.在Grocery上训练SComGNN (w/o m)示例:
```
python run.py --dataset Grocery --lr 0.04 --mode low
```
4.在Home数据集上训练ScomGNN (w/o l)示例:
```
python run.py --dataset Home --lr 0.04 --mode mid

		


