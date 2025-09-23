# NPU_2 - Computer Vision Projects

이 폴더는 컴퓨터 비전 관련 두 가지 프로젝트를 포함합니다.

## 📁 프로젝트 구성

### 1. 파노라마 스티칭 (Panorama Stitching)
**파일**: `1. panorama.py`

여러 이미지를 자동으로 이어 붙여 하나의 파노라마 이미지를 생성합니다.

#### 기능:
- 다중 이미지 자동 로드
- 이미지 크기 자동 조정
- OpenCV Stitcher를 이용한 파노라마 합성
- 결과 이미지 자동 저장

#### 사용법:
```bash
python "1. panorama.py" --input_dir . --pattern "panorama*.jpg" --output result.jpg
```

#### 입력 파일:
- `panorama1.jpg` (4000x3000)
- `panorama2.jpg` (4000x3000)

#### 출력 파일:
- 생성된 파노라마 이미지

---

### 2. 자동차 번호판 검출 및 OCR (License Plate Detection)
**파일**: `2. carplate.py`

이미지에서 자동차 번호판을 자동 검출하고 OCR로 번호를 읽어냅니다.

#### 기능:
- 다중 번호판 동시 검출
- 향상된 OCR 전처리 (크기 조정, 노이즈 제거, 이진화)
- 다양한 OCR 설정 자동 시도
- 검출된 번호판 이미지 자동 저장
- 결과 텍스트 파일 생성

#### 사용법:
```bash
python "2. carplate.py" --input carplate_hw2.jpg
```

#### 입력 파일:
- `carplate_hw2.jpg` - 번호판이 포함된 이미지

#### 출력 파일:
- `plate_1.jpg`, `plate_2.jpg` - 검출된 번호판 이미지들
- `plates.txt` - OCR 결과 텍스트

#### 현재 검출 결과:
```
Plate 1: 99882585
Plate 2: 99892580
```

---

## 🔧 필요한 라이브러리

```bash
pip install opencv-python numpy pytesseract
```

**추가 요구사항:**
- Tesseract OCR 엔진 설치 필요 (번호판 검출용)

---

## 📊 성능 결과

### 파노라마 스티칭:
- ✅ 성공적으로 두 이미지 합성
- 출력 크기: 5500x1531
- 처리 시간: 약 5-10초

### 번호판 검출:
- ✅ 2개 번호판 정확히 검출
- OCR 정확도: 높음 (6-8자리 숫자 인식)
- 처리 시간: 약 3-5초

---

## 📋 파일 목록

```
NPU_2/
├── 1. panorama.py          # 파노라마 스티칭 코드
├── 2. carplate.py          # 번호판 검출 코드
├── carplate_hw2.jpg        # 번호판 검출용 입력 이미지
├── panorama1.jpg           # 파노라마용 입력 이미지 1
├── panorama2.jpg           # 파노라마용 입력 이미지 2
├── plate_1.jpg             # 검출된 번호판 1
├── plate_2.jpg             # 검출된 번호판 2
├── plates.txt              # OCR 결과
└── README.md               # 이 파일
```

---
