# Tensorflow

## 1. 아나콘다 및 CUDA 설치
### 1.1 아나콘다 설치
사이트 접속 후 파일 다운로드
* 사이트: https://repo.continuum.io/archive/index.html
* 다운로드 파일명: Anaconda3-4.2.0 windows-x86_64.exe
* 설치 진행: 별다른 설정 없이 설치하면 됩니다.

### 1.2 CUDA 및 cuDNN 설치(설치하는 장치에 NVIDIA GPU가 있는 경우만 진행)
#### 1.2.1 CUDA 설치
 * 사이트: https://developer.nvidia.com/cuda-downloads
 * 사이트 접속 후 운영체제 선택 > 운영체제 버전 선택 > Installer Type “exe(local)”로 선택 > Base Installer 다운로드
 * 예) Window 선택 > 10 선택 > “exe(local)” 선택 > Base Installer Download
 * 설지 진행: 별다른 설정 없이 설치하면 됩니다.

#### 1.2.2 cuDNN 설치
 * 사이트: https://developer.nvidia.com/cudnn
 * Download 버튼 클릭 > 로그인(가입이 필요함) > 설문조사 후 넘어감 > 라이선스 동의 클릭 > 여러 버전 중 “Download cuDNN v5.1 (Jan 20, 2017), for CUDA 8.0” 클릭 > 운영체제에 맞는 Library 다운로드
 * 다운로드 한 압축 파일을 앞서서 설치한 CUDA 설치경로에 있는 파일에 덮어쓰기 해야 합니다.
 * CUDA 설치 경로: C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v8.0
 * 위 설치 경로로 이동해서 파일들을 복사/붙여넣기 진행

-----------
## 2.	아나콘다에 가상환경 설정
### 2.1 cmd 접속 후 가상환경 구축 명령어 입력
```
conda create -n tensorflow35 python=3.5 anaconda
```
B.	설치가 종료되면 아래와 같이 명령어 입력(GPU 버전은 CUDA 설치했을 때만)
i.	pip install tensorflow-gpu
ii.	pip install tensorflow
C.	설치 후에 아래 명령어를 입력했을 때 목록에 있으면 설치가 제대로 된 것 입니다. 
i.	pip freeze
D.	아래 명령어를 쳐서 현재 tensorflow가 설치된 위치 확인
i.	pip show tensorflow-gpu
ii.	pip show tensorflow
E.	pip show를 했을 때 나온 내용 중 “Location:” 뒤에 나타난 설치 경로 확인
i.	이후에 tensorflow 가상환경 진입 후에 해당 위치로 이동해야 합니다.
F.	설치가 잘 진행되었다면, 아래와 같이 명령어 입력 (cd 이후에 입력하는 설치 경로는 위에서 언급한 location 뒤에 나타나는 설치 경로를 입력해야 합니다.)
i.	Activate tensorflow35
ii.	cd c:\users\nife7\anaconda3\lib\site-packages
iii.	python
iv.	import tensorflow as tf
v.	hello = tf.constant(“Hello World!”)
vi.	sess = tf.Session()
vii.	print(sess.run(hello))

