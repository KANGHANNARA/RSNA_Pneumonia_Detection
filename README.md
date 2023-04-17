# LungObjectDetection_yolov5

RSNA Pneumonia Detection Challenge 흉부 X-ray 이미지에서 599개의 데이터 세트를 라벨링한 후 yolov5 object-detection을 학습

# labeling

동료의 라벨링에 감사드립니다.

"I obtained the dataset, provided with the lowest permission information, through the RSNA Pneumonia Detection Challenge hosted on Kaggle. I sampled 200 images for each label (total 600) from the provided training set and annotated the lungs myself as a nurse. However, please note that the annotations may not be academically reliable, as I am not a radiology specialist."

<img width='30%' src='https://user-images.githubusercontent.com/62852426/228876726-9fd8e419-e893-4150-ab65-eacff745df12.png'/>



yolov5_lung.ipynb 파일은 훈련모델링 노트북입니다.

<img width='100%' src = 'https://user-images.githubusercontent.com/62852426/228880768-8f965ecf-9c51-41c3-9a4f-aed952fd0fd4.png'/>

위의 yolov5 Lung image의 바운딩박스를 crop하여 u-net baseline segmentation을 적용하였습니다.
다음은 캐글노트북 링크입니다.
https://www.kaggle.com/code/score42/lung-segmentation-from-chest-x-ray-dataset/notebook

<img width='100%' src = 'https://user-images.githubusercontent.com/62852426/230782809-24814476-718a-4b25-a22f-29c83b8c7a9f.png'/>

왼쪽이 test 가운데가 test_mask 오른쪽이 predict_image
<img width='100%' src = 'https://user-images.githubusercontent.com/62852426/230782872-5fd983b1-34cc-4c61-902d-2d1ed3921415.png'/>
