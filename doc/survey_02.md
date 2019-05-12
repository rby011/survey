# Guided, Stochastic Model-Based GUI Testing of Android Apps

* ESEC/FSE 2017 Proceedings of the 2017 11th Joint Meeting on Foundations of Software Engineering

* [fse17-stoat-full-paper.pdf](../resources/fse17-stoat-full-paper.pdf)

* https://github.com/tingsu/Stoat

## KeyWord

* Stochastic Behavior Model, GUI Testing

## Summary

* 어플리케이션 상태 변화를 가중치 그래프 모델로 표현, node 는 UI Widget 의 상태로 edge 는 출현 빈도로 정의

* 도구 수행은 1) 초기 모델 구축 단계와 2) 모델 뮤테이션 단계로 구성되고 단계-2 에서 Test Sequence 생성 및 수행

* 단계-1 에서는 정적 분석을 통해 어플리케이션 별로 의미있는 사용자 이벤트 집합과 관심 이벤트 집합을 도출하는 것,

* 또한 시스템 이벤트를 단계-2 에서 상태와 무관하게 주입해주는 것도 Crash(#) 와 Code Coverage 개선에 큰 역할.

* SOTA 였던 Facebook Sapienz 을 Crash Uniqueness 와 Code Coverage 기준으로 추월했다는 점에서 눈여겨 볼 만함

  * 이들 GUI 테스트 자동화 영역은 Unique Crash (#), Coverage 기준을 가지고 대결 中

* 강화 학습의 구조와 매우 유사한 구조와 알고리즘을 가지고 있음. *Stoat 것을 벤치마킹해서 강화학습으로 변경해서 개선한다면?*

  * learning : model construction phase

  * model + Q function = application model

  * policy = gib sampling , reward = objective function
