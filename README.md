# LungObjectDetection_yolov5

RSNA Pneumonia Detection Challenge 흉부 X-ray 이미지에서 599개의 데이터 세트를 라벨링한 후 yolov5 object-detection을 학습한 가중치를 공유하는 레포지토리 입니다.

# labeling

동료의 라벨링에 감사드립니다.

"I obtained the dataset, provided with the lowest permission information, through the RSNA Pneumonia Detection Challenge hosted on Kaggle. I sampled 200 images for each label (total 600) from the provided training set and annotated the lungs myself as a nurse. However, please note that the annotations may not be academically reliable, as I am not a radiology specialist."

![228791194-9aa3775f-0ac7-4c9c-a6bf-380e90e0d04b](https://user-images.githubusercontent.com/62852426/228876726-9fd8e419-e893-4150-ab65-eacff745df12.png)

"I converted the DICOM format to a 1024x1024 PNG format and used the 'Label-Studio' tool to annotate the lungs as shown below. I marked the highest part of the upper lobe, the lowest part of the lower lobe, and the widest part of the lungs from side to side."

# Lung_detection.pt 가중치의 링크입니다.

https://drive.google.com/file/d/10Hdiz1DGhlQ_pF6pl3HhW-n7F7nIN0UZ/view?usp=share_link
