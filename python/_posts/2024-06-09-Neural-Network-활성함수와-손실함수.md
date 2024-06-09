---
layout: post
title: 20240609_Neural Network_활성함수와 손실함수
description: >
  뉴럴네트워크란 입력값과 예측(결과)값 사이에 신경망(hidden-layer)가 있어서 사람처럼 생각하면서 예측할 수 있게 해주는거
sitemap: false
hide_last_modified: true
---

# 20240609_Neural Network?

- ![](/assets\img\python\Clipboard_2024-06-09-19-08-06.png)

- 뉴럴네트워크란 입력값과 예측(결과)값 사이에 신경망(hidden-layer)가 있어서 사람처럼 생각하면서 예측할 수 있게 해주는거

## 활성함수 (activation function)
- 결과값을 예측할 때 hidden layer의 각 노드들의 연산 결과를 예측에 활용할 수 있게(의미있게) 변형시켜주는 함수
    - 이를 활용해서 선형적인 단순한 예측에서 비선형적이고 복잡한 예측을 가능하게 해준다.
- 활성함수의 종류 : hyperbolic tangent, sigmoid, softmax, rectified linear...
    - ex) 시그모이드 함수 : x에 hidden layer node 값을 넣어서 계산하면 0에서 1 사이의 값으로 압축시켜줌 (0을 집어넣으면 0.5가 나옴)
    - ![](/assets\img\python\Clipboard_2024-06-09-19-11-56.png)
    - ![](/assets\img\python\Clipboard_2024-06-09-19-14-19.png)
    - 이미지출처 : https://nongnongai.tistory.com/54

## 예측모델의 오차를 구하는 방법

- 존재하는 데이터를 기준으로(실제값,결과값) 오차를 최소하하는 가중치를 찾아야함(컴퓨터가 찾음. 다만 가중치를 찾는 기준을 정확히 명령해줘야 함)

### 손실함수 (Loss function)

- 총 오차를 계산하는 수식을 손실함수라고 부르며, 상황에 따라 다양한 수식이 있음
    - 예측값 - 결과값을 제곱해서 평균치를 구하는 방식도 있음(양수,음수따문에 )