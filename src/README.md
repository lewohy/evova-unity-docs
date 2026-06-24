# Introduction

[EVOVA](https://www.evova.ai) Unity Plugin 공식 문서입니다.

<p align="center">
    <video width="80%" height="auto" controls autoplay loop>
        <source src="./assets/videos/introduction.mp4" type="video/mp4">
    </video>
</p>

<p align="center">
    <video width="80%" height="auto" controls autoplay loop>
        <source src="./assets/videos/demo1.mp4" type="video/mp4">
    </video>
</p>

## 개요

이 플러그인은 Vanilla 3DGS(3D Gaussian Splatting) Scene의 데이터 구조를 그대로 유지하면서, 추가 학습 없이 실시간 라이팅 효과를 구현하는 것을 목표로 합니다.

[aras-p/UnityGaussianSplatting](https://github.com/aras-p/UnityGaussianSplatting) 플러그인을 기반으로 만들어졌으며, Unity URP(Universal Render Pipeline) 환경에서 동작합니다. 사용된 다른 프로젝트에 대한 내용은 [License 페이지](./license.md)를 참고하세요.

저희는 3DGS 생태계의 발전에 도움을 주고자 이 플러그인을 무료로 배포하고 있습니다.

## 주요 특징

- 3DGS Scene의 normal 추정을 통한 Directional Light 라이팅
- depth 추론을 응용한 shadow casting
- 원본 3DGS 에셋 구조를 변경하지 않는 비파괴적 접근

> **참고:** 이 플러그인은 매우 실험적인 접근 방식을 사용합니다. 3DGS 에셋의 종류와 특성에 따라 조명 효과가 달라질 수 있습니다. 자세한 내용은 [Usage](guide/usage.md)와 [Troubleshooting](guide/troubleshooting.md)을 참고하세요.

## 시작하기

아래 가이드를 따라주세요

1. [Installation](guide/installation.md) — 플러그인 설치
2. [Setup](guide/setup.md) — 초기 설정
3. [Usage](guide/usage.md) — 3DGS 에셋 생성 및 렌더링
4. [Troubleshooting](guide/troubleshooting.md) — 알려진 문제 해결
5. [Features](guide/features.md) — 구현된 기능 및 로드맵
