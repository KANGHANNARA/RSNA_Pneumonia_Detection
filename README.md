# LungObjectDetection_yolov5

RSNA Pneumonia Detection Challenge 흉부 X-ray 이미지에서 599개의 데이터 세트를 라벨링한 후 yolov5 object-detection을 학습한 가중치를 공유하는 레포지토리 입니다.

# labeling

동료의 라벨링에 감사드립니다.

"I obtained the dataset, provided with the lowest permission information, through the RSNA Pneumonia Detection Challenge hosted on Kaggle. I sampled 200 images for each label (total 600) from the provided training set and annotated the lungs myself as a nurse. However, please note that the annotations may not be academically reliable, as I am not a radiology specialist."

<img width='30%' src='https://user-images.githubusercontent.com/62852426/228876726-9fd8e419-e893-4150-ab65-eacff745df12.png'/>

"I converted the DICOM format to a 1024x1024 PNG format and used the 'Label-Studio' tool to annotate the lungs as shown below. I marked the highest part of the upper lobe, the lowest part of the lower lobe, and the widest part of the lungs from side to side."

# Lung_detection.pt 가중치의 링크입니다.

https://drive.google.com/file/d/10Hdiz1DGhlQ_pF6pl3HhW-n7F7nIN0UZ/view?usp=share_link

# 사용하는 방법

이 모델은 YOLOv5를 기반으로 하므로 먼저 YOLOv5 리포지토리를 복제해야 합니다:https://github.com/ultralytics/yolov5.git

```
$ git clone https://github.com/ultralytics/yolov5.git
```

다음으로 Lung_detection.pt 가중치를 다운로드하고 권장 경로에 배치합니다.

```
…/yolov5/models/lung_detection.pt
```

이제 yolov5 를 사용하여 Lung object detection을 사용할 수 있습니다. 자세한 내용은 yolov5 리포지토리를 참고하세요.:https://github.com/ultralytics/yolov5.git
```
$ cd .../yolov5
$ python detect.py --weight [weighs path] --source [object directory] --save-txt
```
이렇게 하면 바운딩 박스 좌표가 포함된 결과 이미지와 텍스트 파일이 생성됩니다. 기본 출력 경로는 yolov5/run/detect/exp입니다.
YOLOv5에서 지원하는 다양한 옵션에 대한 자세한 내용은 YOLOv5 리포지토리를 참고하세요.

yolov5_lung.ipynb 파일은 훈련모델링 노트북입니다.

<img width='100%' src = 'https://user-images.githubusercontent.com/62852426/228880768-8f965ecf-9c51-41c3-9a4f-aed952fd0fd4.png'/>

위의 yolov5 Lung image의 바운딩박스를 crop하여 u-net baseline segmentation을 적용하였습니다.
다음은 캐글노트북 링크입니다.
https://www.kaggle.com/code/score42/lung-segmentation-from-chest-x-ray-dataset/notebook
<img width='100%' src = 'https://user-images.githubusercontent.com/62852426/230782809-24814476-718a-4b25-a22f-29c83b8c7a9f.png/>
