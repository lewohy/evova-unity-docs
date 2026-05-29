---
layout: post
title: 3DGS Plugin for Unity
date: 2026-05-29 14:19 +0900
---

리라이팅이 가능한 유니티용 3DGS 플러그인
[aras-p의 3DGS 플러그인](https://github.com/aras-p/UnityGaussianSplatting)을 기반으로 만들어졌습니다.

## Installation

현재 소스코드는 제공되지 않으며 Unity DLL파일로 제공됩니다.


## 변경사항

- 유니티 오브젝트보다 뒤에 있는 3DGS Scene이 가려지지 않고 계속 보이는 문제를 해결합니다.
- 유니티 내의 광원과 상호작용이 가능하도록 개선합니다.

## Usage



### 주의사항

해당 플러그인은 개발 단계에 있어서 명확한 한계가 존재합니다

- 단일 Directional Light에서만 의도한대로 작동합니다.
- 라이팅을 적용하기 위해 shadow map에 크게 의존합니다. 이 때문에 shadow map의 해상도가 충분하지 않으면 올바른 라이팅이 적용되지 않습니다.

> 해당 문제점은 개선 계획에 있습니다. 현재는 컴퓨터의 사양과 퀄리티에 타협하여 사용해야합니다

두 가지 shadow map의 해상도를 올리는 방법이 있습니다.

**Shadow Resolution**
- 렌더링하는 실제 shadow map의 해상도를 높입니다.
> 최대로 올리면 부하가 심해집니다. 특정 오브젝트에 대한 해상도를 극적으로 올리기에는 부족합니다.

**Shadows - Max Distance**
- 렌더링하는 shadow map의 범위를 줄입니다.
> 체감되는 shadow map의 해상도 차이가 큽니다. 단 비교적 가까운 거리의 그림자가 제대로 렌더링 되지 않을 수 있습니다.

우리는 이 단점을 이후 Cascading Shadow 방식을 지원하도록 하여 개선하도록 할 예정입니다.



## 계획

- [x] 표면과 빛의 입사각에 따른 빛 반사 반영
- [x] 3DGS Scene에 Unity Object의 그림자 캐스팅
- [ ] Cascading Shadow 지원
- [ ] 반사 표면에 대한 처리
