# MyTorch
Paper reproductions &amp; idea implementations.

# ⚡프로젝트 개요
- 딥러닝 모델 구현 프로젝트 (PyTorch, Lightning)
- 실력 향상 및 현재 연구 분야의 이해 향상을 위해 최신 논문을 재현하고 실험을 수행함.
- 실력 향상을 위해 논문에 실리지는 않았지만 연구 수행 초기 단계에 떠오른 아이디어들을 구현해봄.

### 1. CADGen: Causal Language Modeling을 활용한 3D 모델 학습 및 생성

- 명령어 시퀀스로 표현된 3D CAD 모델에 대해 GPT와 같은 next token prediction을 수행하는 causal language modeling (CLM) 방식으로 학습할 수 있도록 **데이터셋을  토큰 시퀀스 형태로 재구성.**
- Transformer LM 모델을 `pytorch`로 구현하고 실험을 수행함.
- `hydra`를 이용해 `yaml` 파일로부터 실험 파라미터들을 효율적으로 관리하고, `wandb`를 이용한 logging을 수행함.
- https://github.com/cm8908/CADGen

### 2. MaskedCAD: Masked Language Modeling을 활용한 3D 모델 학습

- CAD 명령어 시퀀스에 대해 일부를 masking하고 이를 예측하는 masked language modeling (MLM) 방식으로 학습할 수 있도록 커스텀 데이터셋을 구축함.
- MLM 방식과 더불어 두 종류의 contrastive learning 방법을 함께 적용하여 학습하는 방법을 구현함.
- https://github.com/cm8908/MaskedCAD

### 3. NETSP: CNN-LSTM 기반논문 구현

- *Sultana et al., Learning to optimise general TSP instances, Int. J. Mach. Learn Cybern., 2022.*
- TSP 데이터에 대해 CNN 임베딩을 사용해 공간정보 학습, LSTM을 이용해 순차적 정보를 학습하는 지도학습 기반 모델.
- `pytorch-lightning`을 이용해 모델을 구현하고 학습을 관리함.
- https://github.com/cm8908/netsp

### 4. TSPXL: Transformer-XL for TSP

- context length 제한으로 인해 학습이 어려웠던 long sequence에 대해 더 효과적으로 학습할 수 있는 Transformer-XL 모델을 구현하고 TSP 데이터에 대해 학습시킴.
- Transformer-XL 모델의 논문과 코드를 읽고 이를 TSP 데이터에 대해 적용하고자 TSP 데이터를 전처리한 뒤 입력받아 모델 학습을 수행하는 파이프라인을 `pytorch`를 이용해 구축하고 `hydra`로 실험 변수를 관리함.
- https://github.com/cm8908/tspxl

### 5. TODO: LLM-based application
