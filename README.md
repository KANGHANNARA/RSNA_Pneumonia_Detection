# yolov5 RSNA_Pneumonia_Detection baseline 

이번 프로젝트의 목적은 모델의 성능의 증가가 아닌 여러가지 task에 여러가지 모델을 적용시켜 

모델 과정을 학습하는 것이 목표입니다.

추가적인 전처리없이 모델 학습을 진행 하였으며 결과물을 제출하는 것까지 진행하였습니다.


<aside>
<img src="/icons/bullseye_gray.svg" alt="/icons/bullseye_gray.svg" width="40px" /> !python **train.py**
--img 416 --batch 16 --epochs 5
--data /content/data.yaml
--cfg /content/yolov5/models/yolov5m.yaml
--weights **yolov5m.pt**
--name /content/drive/MyDrive/Pneumonia_model1_5peochs

</aside>



# LungObjectDetection_yolov5

RSNA Pneumonia Detection Challenge 흉부 X-ray 이미지에서 599개의 데이터 세트를 라벨링한 후 yolov5 object-detection을 학습 yolov5_lung.ipynb 이 Lung object detection 입니다.

# labeling

동료의 라벨링에 감사드립니다.

"I obtained the dataset, provided with the lowest permission information, through the RSNA Pneumonia Detection Challenge hosted on Kaggle. I sampled 200 images for each label (total 600) from the provided training set and annotated the lungs myself as a nurse. However, please note that the annotations may not be academically reliable, as I am not a radiology specialist."

<img width='30%' src='https://user-images.githubusercontent.com/62852426/228876726-9fd8e419-e893-4150-ab65-eacff745df12.png'/>



yolov5_lung.ipynb 파일은 훈련모델링 노트북입니다.

<img width='100%' src = 'https://user-images.githubusercontent.com/62852426/228880768-8f965ecf-9c51-41c3-9a4f-aed952fd0fd4.png'/>

위의 yolov5 Lung image의 바운딩박스를 crop하여 u-net baseline segmentation을 적용하였습니다.
다음은 캐글노트북 링크입니다.
https://www.kaggle.com/code/score42/lung-segmentation-from-chest-x-ray-dataset/notebook
위의 파일에서 lung-segmentation-from-chest-x-ray-dataset.ipynb 이 캐글노트북 파일입니다.

<img width='100%' src = 'https://user-images.githubusercontent.com/62852426/230782809-24814476-718a-4b25-a22f-29c83b8c7a9f.png'/>

왼쪽이 test 가운데가 test_mask 오른쪽이 predict_image
<img width='100%' src = 'https://user-images.githubusercontent.com/62852426/230782872-5fd983b1-34cc-4c61-902d-2d1ed3921415.png'/>
