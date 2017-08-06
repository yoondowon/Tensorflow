# Tensorflow

## 1. 아나콘다 및 CUDA 설치
### 아나콘다 다운로드
사이트 접속 후 파일 다운로드
* 사이트: https://repo.continuum.io/archive/index.html
* 다운로드 파일명: Anaconda3-4.2.0 windows-x86_64.exe
* 설치 진행: 별다른 설정 없이 설치하면 됩니다.

### CUDA 및 cuDNN 다운로드(설치하는 장치에 NVIDIA GPU가 있는 경우만 진행)
#### CUDA 사이트 접속 후 파일 다운로드
 * 사이트: https://developer.nvidia.com/cuda-downloads
 * 사이트 접속 후 운영체제 선택 > 운영체제 버전 선택 > Installer Type “exe(local)”로 선택 > Base Installer 다운로드
 * 예) Window 선택 > 10 선택 > “exe(local)” 선택 > Base Installer Download
 * 설지 진행: 별다른 설정 없이 설치하면 됩니다.

#### cuDNN 사이트 접속 후 파일 다운로드
 * 사이트: https://developer.nvidia.com/cudnn
 * Download 버튼 클릭 > 로그인(가입이 필요함) > 설문조사 후 넘어감 > 라이선스 동의 클릭 > 여러 버전 중 “Download cuDNN v5.1 (Jan 20, 2017), for CUDA 8.0” 클릭 > 운영체제에 맞는 Library 다운로드
 * 다운로드 한 압축 파일을 앞서서 설치한 CUDA 설치경로에 있는 파일에 덮어쓰기 해야 합니다.
 * CUDA 설치 경로: C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v8.0
 * 위 설치 경로로 이동해서 파일들을 복사/붙여넣기 진행
