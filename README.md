# her2-gene-expression
data from Farahmand, Saman, Fernandez, Aileen I, Ahmed, Fahad Shabbir, Rimm, David L., Chuang, Jeffrey H., Reisenbichler, Emily, & Zarringhalam, Kourosh. (2022). HER2 and trastuzumab treatment response H&E slides with tumor ROI annotations (Version 3) [Data set]. The Cancer Imaging Archive. https://doi.org/10.7937/E65C-AM96

Confirm her2 gene expression with her2 tumor data/expecting results of tranzmap treatment

Overfitting has been sovled after I decreasd the learning rate into 0.01->0.0001 and changed the optimizer to SGD->Adam

I made a mistake in  her2학습.ipynb. The patch from each patients were randomly inserted into train and val files without first deciding where to put the patient in training or val folder, and it seems that the oscillation was severe because of this.
# Distinguishing between positive and negative responses to Trastuzumab
#### Comparison of performance between training on patches from whole slide images and patches from tumor regions only
For trantuzmap data, I first used pretrained rsnet 18, but the overfitting kept occured, and I thought the model was too deep for my dataset, so I changed into two layer cnn.
 
 
### 패치 단위 학습 외에도   Sliding Window 기반 학습/예측 같은 걸로 학습하면 정확도 더 높일 수 있다고 하셔서 자세히 찾아보기
