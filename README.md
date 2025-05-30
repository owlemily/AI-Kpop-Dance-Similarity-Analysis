
# 🕺 AI 기반 K-pop 안무 유사도 분석 시스템
- 2025학년도 상명대학교 빅데이터융합학부 **모션캐쳐s** 팀의 캡스톤디자인 작품입니다.
- ASK 2025 "ViTPose기반 K-pop 안무 동작의 유사도 측정에 관한 연구" 게재 수락


## 📌 프로젝트 개요
이 프로젝트는 K-pop 안무 영상 두 개를 비교하여, 동작의 유사도를 AI 기반으로 분석하는 시스템입니다.
ViTPose 모델을 사용해 사람의 관절(keypoints)을 추정하고, 정렬 및 유사도 측정을 통해 두 안무의 동작 유사성을 시각적으로 분석합니다.

## 🔁 분석 흐름
1. 라이브러리 설치 및 import
2. ViTPose 모델 로드
3. 두 안무 영상 전처리
   - 영상 길이 일치
   - FPS 동기화
4. Keypoints 추출
5. Keypoints 정규화
6. DTW(Dynamic Time Warping)를 통한 프레임 정렬
7. 관절 중요도를 반영한 Weighted Cosine Similarity 계산
8. 시각화
  - Skeleton 시각화
  - 유사도 시각화
  - 영상 합성

## 사용 방법
Google Colab에서 .ipynb 파일을 실행하면 전체 파이프라인을 단계별로 확인할 수 있습니다.
사용자 지정 영상만 넣으면 자동으로 유사도 분석이 진행됩니다.

📦 주요 기술
- Pose Estimation: ViTPose Transformer
- 시계열 정렬: DTW (Dynamic Time Warping)
- 유사도 측정: 가중치 기반 Cosine Similarity
- 시각화: OpenCV + Skeleton Overlay
