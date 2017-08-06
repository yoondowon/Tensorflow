# Tensorflow

## 1. 아나콘다 및 CUDA 설치
### 1.1 아나콘다 설치
사이트 접속 후 파일 다운로드
* 사이트: https://repo.continuum.io/archive/index.html
* 다운로드 파일명: Anaconda3-4.2.0 windows-x86_64.exe
* 설치 진행: 별다른 설정 없이 설치하면 됩니다.

### 1.2 CUDA 및 cuDNN 설치
설치하는 장치에 NVIDIA GPU가 있는 경우만 진행합니다.

#### 1.2.1 CUDA 설치
 * 사이트: https://developer.nvidia.com/cuda-downloads
 * 사이트 접속 후 운영체제 선택 > 운영체제 버전 선택 > Installer Type “exe(local)”로 선택 > Base Installer 다운로드
 * 예) Window 선택 > 10 선택 > “exe(local)” 선택 > Base Installer Download
 * 설 진행: 별다른 설정 없이 설치하면 됩니다.

#### 1.2.2 cuDNN 설치
 * 사이트: https://developer.nvidia.com/cudnn
 * Download 버튼 클릭 > 로그인(가입이 필요함) > 설문조사 후 넘어감 > 라이선스 동의 클릭 > 여러 버전 중 “Download cuDNN v5.1 (Jan 20, 2017), for CUDA 8.0” 클릭 > 운영체제에 맞는 Library 다운로드
 * 다운로드 한 압축 파일을 앞서서 설치한 CUDA 설치경로에 있는 파일에 덮어쓰기 해야 합니다.
 * CUDA 설치 경로: C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v8.0
 * 위 설치 경로로 이동해서 파일들을 붙여넣기 합니다.

## 2.	Tensorflow 설치 및 테스트
### 2.1 가상환경 생성
cmd 접속 후 아래와 같이 입력합니다.
```
conda create -n tensorflow35 python=3.5 anaconda
```

### 2.2 Tensorflow install 
GPU 버전은 CUDA 설치했을 때만 install 합니다.
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
아래 명령어를 쳐서 현재 tensorflow가 설치된 위치를 확인합니다.

Location: 뒤에 나타나는 경로가 설치된 경로입니다. (이후에 tensorflow 가상환경 진입 후에 해당 위치로 이동해야 합니다.)
```
pip show tensorflow-gpu
pip show tensorflow
```

### 2.5 Tensorflow Test
아래와 같이 입력하여 "Hello World"가 나타나면 제대로 진행된 것 입니다. 

cd 이후에 입력하는 설치 경로는 위에서 언급한 location 뒤에 나타나는 설치 경로를 입력해야 합니다.

sess 입력 후에 나타나는 메시지는 무시하시고 진행하면 됩니다.
```
Activate tensorflow35
cd c:\users\user\anaconda3\lib\site-packages
python
>>> import tensorflow as tf
>>> hello = tf.constant(“Hello World!”)
>>> sess = tf.Session()
>>>	print(sess.run(hello))
```

### 2.6 Path 설정
매번 가상환경에서 cd로 경로를 입력하기 어렵기 때문에 path 설정을 해줍니다.

path 설정 후에는 위의 코드에서 cd 코드는 입력하지 않아도 됩니다. 
 * 내컴퓨터 우클릭 > 고급 시스템 설정 > 환경변수 > 시스템변수에 있는 변수 중 Path 클릭 후 편집 > 새로만들기 > 경로 입력 후 확인

## 3. Pycharm에서 Tensorflow 사용
### 3.1 Pycharm 설치
 * 사이트: https://www.jetbrains.com/pycharm/download/#section=windows
 * Coummunity Version으로 다운로드합니다.
 
### 3.2 Pycharm 설정
 * New Project 클릭 후 Interpreter 우측의 톱니바퀴 아이콘을 클릭한 후 Add Local를 클릭합니다.
 * c:\users\ ... \anaconda3\envs 로 이동하면 앞서 구성한 tensorflow35 폴더가 보입니다.
 * tensorflow35 폴더내에있는 python.exe를 클릭 후 OK를 클릭합니다.
 * create 클릭합니다.
 * Pycharm에서 File > Settings > Project:your_project_name > Project Interpreter로 이동합니다.
 * 우측에있는 + 아이콘을 클릭한 후 tensorflow를 검색하여 설치합니다.
 * 위와 동일한 코드를 실행하여 설정이 완료되었는지 확인합니다.
 
```
import tensorflow as tf

hello = tf.constant(“Hello World!”)
sess = tf.Session()
print(sess.run(hello))
```



