## Brain-to-Music : Implementation of EEG-based user-friendly music composition algorithm

사용자의 깊은 내면에 숨겨져 있는 자신의 감정을 음악으로 표현하여, 자신의 내면을 들여다 볼 수 있도록 하기 위해서 EEG Data를 이용해 음악을 작곡하는 알고리즘을 개발하였다.

EEG 데이터를 통해 감정에 맞는 음악을 작곡하는 알고리즘 모델 개발하고, 이를 통해 작곡한 음악과, 실험자들의 감정이 가지는 상관관계 평가한다.
앞서 만들어진 음악을 사용자가 원하는 악기로 변환하고 이 과정을 GUI로 구현하는 프로젝트를 진행하였다. 




<img src="https://img.shields.io/badge/numpy-1.19.5-yellowgreen"/> 
<img src="https://img.shields.io/badge/pandas-1.2.0-yellowgreen"/> 
<img src="https://img.shields.io/badge/scipy-1.5.4-yellowgreen"/> 
<img src="https://img.shields.io/badge/pyeeg-0.0.2-yellowgreen"/> 
<img src="https://img.shields.io/badge/pycaret-2.3.4-red"/> 
<img src="https://img.shields.io/badge/pretty_midi-0.2.9-red"/> 
<img src="https://img.shields.io/badge/pyqt-5.9.2-blue"/>







- **GUI** : Graphic User Interface를 사용하기 위한 코드가 들어있고, PyQT를 이용하여 제작을 했다.
- **code**  :
    - **application.py** : application을 실행시키는 Main File
    - convert_signal_to_music.py : 뇌파 신호를 음악으로 변환하기 위한 알고리즘을 구현한 코드
    - emotion_analysis_model.py : 학습된 모델을 이용하여 뇌파의 감정을 분석하기 위한 코드
    - feature_extractor.py : 뇌파에서 다양한 feature를 추출하기 위한 코드

- **model** : 감정분석을 위해 뇌파 데이터에서 추출한 Feature를 이용하여 Arousal과 Valence를 각각 예측하는 이진 분류 기계학습 모델
- **music** : Application을 이용해 뇌파를 음악으로 변환한 Sample midi file
- **music_control_feature** :
    - high/low_kurtosis : Volume을 조절하기 위해 기존 데이터에서 Kurtosis를 분석한 결과





### 실행방법 : 

1. EEG Data를 상단의 Box에 Drag and Drop 
2. `Extract Feature`를 통해서 EEG Data에서 필요한 특성들을 추출 
3. `Emotion Analysis`를 통해서 현재 사용자의 EEG Data에 대한 Arousal과 Valence 예측
4. 좌측 하단에서 사용자가 원하는 악기를 선택 
5. `Convert Signal to Music`를 통해서 EEG Data를 이용하여 Midi File 생성 및 저장
6. `Reset` 버튼을 통해서 기존의 내용을 초기화 


