## 프로젝트 개요

- Tracking 하고자 하는 객체가 학습된 YOLO의 Object detection이 아니라, 현장에서 즉시 대응 가능해야하는 경우를 가정
- 사용자가 Tracking하고자 하는 객체를 선택하면 그것을 시각적 tracking을 해주는 프로그램
- 추가로, 그 tracking 결과를 기반으로 YOLO 학습을 위한 라벨링을 자동으로 하도록 구현하는 코드도 추가 해봄

## 주요 기능

- CSRT 알고리즘을 활용한 Tracker 구현, 결과는 마치 YOLO와 같이 bbox를 그림
- Tracking 결과에 대해 bbox 좌표를 정규화된 값으로 외부로 mqtt 프로토콜로 송신하는 기능
- input source의 사이즈를 resize하여 연산량을 줄이도록 구현
- Auto label이라는 이름으로, tracking 한 결과를 임의의 시간 주기로 이미지와 annotation 정보를 txt로 저장하도록 함

## ⚙️ 환경 설정
- pip install -r requirements.txt
- Python 3.11

## 🎥 결과물 (Demo)
<p align="center">
<img src="util/output_tracking.gif" width="90%">
</p>