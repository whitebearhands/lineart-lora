# LoRA 학습 프로젝트: Lineart Style LoRA

이 프로젝트는 Stable Diffusion v1.5 베이스 모델에 LoRA (Low-Rank Adaptation)를 학습시켜 특정 라인아트 스타일의 이미지를 생성하는 방법을 보여줍니다.

## 모델 정보

*   **베이스 모델**: `runwayml/stable-diffusion-v1-5`
*   **학습 목표**: 이미지를 라인아트 스타일로 변환하거나 해당 스타일의 이미지를 생성하는 LoRA 모델 학습
*   **트리거 워드**: `lineart_style` (이 단어를 프롬프트에 포함하여 학습된 스타일을 활성화합니다.)

## LoRA 학습 파라미터

이 LoRA 모델은 다음 주요 파라미터로 학습되었습니다.

*   **해상도 (`resolution`)**: `512`x`512` 픽셀
*   **최대 학습 스텝 (`max_train_steps`)**: `5000` 스텝
*   **학습 배치 크기 (`train_batch_size`)**: `4` (실질 배치 크기: `8`)
*   **그라디언트 누적 스텝 (`gradient_accumulation_steps`)**: `2`
*   **학습률 (`learning_rate`)**: `1e-4`
*   **LoRA 랭크 (`rank`)**: `64` (LoRA 가중치의 복잡성 조절)
*   **LoRA 알파 (`alpha`)**: `32` (LoRA 가중치 스케일링)
*   **체크포인팅 스텝 (`checkpointing_steps`)**: `500` 스텝마다 모델 저장
*   **혼합 정밀도 (`mixed_precision`)**: `fp16` (메모리 효율성 증대)
*   **옵션**: XFormers 메모리 효율적 어텐션 활성화 (`enable_xformers_memory_efficient_attention`)

## Hugging Face Hub 정보

학습된 LoRA 모델은 Hugging Face Hub에서 확인할 수 있습니다.

*   **리포지토리 ID**: `whitebearhands/lineart-lora`
*   **링크**: [https://huggingface.co/whitebearhands/lineart-lora](https://huggingface.co/whitebearhands/lineart-lora)

## 기여자

[이 프로젝트에 기여한 사람들의 이름을 나열하세요.]
