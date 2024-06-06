---
layout: post
title: Tensorflow 2 개발환경 셋팅 (윈도우)
description: >
  텐서플로우2 개발환경 셋팅 방법 기록
sitemap: false
hide_last_modified: true
---

# 20240606_Tensorflow 2 개발환경 셋팅 (윈도우)

## 텐서플로우란?
- 구글개발자들이 만든 딥러닝을 매우 쉽게 구현할 수 있게 해주는 파이썬 라이브러리

## 텐서플로우 설치
- 공식사이트 : https://www.tensorflow.org/install?hl=ko
### 1. 파이썬 설치
- 내 버전 : Python 3.12.2 (tags/v3.12.2:6abddd9, Feb  6 2024, 21:26:36) [MSC v.1937 64 bit (AMD64)] on win32
### 2.텐서플로우 라이브러리 설치

``` python
# Requires the latest pip
pip install --upgrade pip

# Current stable release for CPU and GPU
pip install tensorflow

# Or try the preview build (unstable)
pip install tf-nightly
```

### 3. 설치확인
- 테스트 파일 생성 후 실행해보기기 (waring GPU CUDA~~ 메시지만 안뜨면 성공)

``` python
import tensorflow as tf
```

### 4. 참고 (딥러닝을 GPU로 돌리는 이유)
- GPU를 사용하면 CPU보다 10~20배 빠르게 작업을 완료할 수 있는데, 딥러닝에 필요한 연산은 99%가 행렬 곱 엽산이고, 이거를 GPU가 잘함
