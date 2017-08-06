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

## 2.	Tensorflow 설치 및 테스트
### 2.1 가상환경 생성
cmd 접속 후 아래와 같이 입력
```
conda create -n tensorflow35 python=3.5 anaconda
```

### 2.2 Tensorflow install (GPU 버전은 CUDA 설치했을 때만)
```
pip install tensorflow-gpu
pip install tensorflow
```

### 2.3 설치 확인
설치 후에 아래 명령어를 입력했을 때 목록에 있으면 설치가 제대로 된 것 입니다. 
```
pip freeze
```

### 2.4 Tensorflow 설치 위치 확인
아래 명령어를 쳐서 현재 tensorflow가 설치된 위치 확인
Location: 뒤에 나타나는 경로가 설치된 경로입니다. (이후에 tensorflow 가상환경 진입 후에 해당 위치로 이동해야 합니다.)
```
pip show tensorflow-gpu
pip show tensorflow
```

### 2.5 Tensorflow Test
설치가 잘 진행되었다면, 아래와 같이 입력하여 "Hello World"가 나타나면 제대로 진행된 것 입니다. 
cd 이후에 입력하는 설치 경로는 위에서 언급한 location 뒤에 나타나는 설치 경로를 입력해야 합니다.
sess 입력 후에 나타나는 메시지는 무시하시고 진행하면 됩니다.
```
Activate tensorflow35
cd c:\users\nife7\anaconda3\lib\site-packages
python
>>> import tensorflow as tf
>>> hello = tf.constant(“Hello World!”)
>>> sess = tf.Session()
>>>	print(sess.run(hello))
```



