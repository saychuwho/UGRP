# Generation of Modular and Measurable Validation Scenarios of Autonomous Vehicles Using Accident Data

## keyword

Autonomous vehicle, AV Crashes, Simulation, Validation, Scenario Generation

## abstract

- 요약 : 
  - *In this paper, we use the existing AV accident data and identify the atomic blocks within each accident, which are modular and measurable scenario units.*
  - accident scenario를 이 atomic block을 이용해 만들고 이를 Measurable Scenario Descriotion Language(M-SDL)로 정의한다.
  - 이러한 접근은 사고 상황 분석이 들어간 modular scenario units을 제공하고, 사고 상황 당시에 자동차의 행동을 측정을 통해 분석할 수 있는 방법을 제공하며, AV assessment metric을 이용한 edge scenaio를 찾을 수 있다.
- 모르는 단어
  - coverage : the reporting of a particular important event or subject.
  - metric : using or relating to a system of measurement that uses metres, centimetres, litres, etx.
## introduction

- 요약
  - 자율주행 자동차가 늘어나면서 이에 대한 사고 상황도 늘어나고, 이는 자율주행 자동차의 발전에 장애물이 되었다.
  - 자율주행 자동차의 corner case에서 버그들을 찾고, 시험 진행 상황은 평가를 위해 투명해야 한다. 여기서 자율주행 자동차 사고는 테스트 및 검증에 사용할 수 있는 귀중한 데이터를 제공한다.
  - 이 페이퍼는 자율주행 모드에서 발생할 수 있는 사고 시나리오를 이용해 자율주행 자동차를 평가할 수 있는 논리적이고 견고한 테스트 시나리오를 만드는 방법론을 제시한다. 
    - 우리의 접근법은 각각의 crash report에 있는 사고 시나리오 속 functional description을 여러개의 추상적인 atomic block으로 나눈다. 그리고 이 block들은 test scenario를 만드는데 modular unit으로 사용된다. 
    - 방법론은 AV의 scenario based validation of decision-making 에 집중한다.
    - 이 방법론은 사고들을 재구성한 테스트 시나리오를 제공하고 이는 Measurable Scenario Descriotion Language로 제공된다.
  - 시나리오를 구성하는 atomic block들은 모듈화되어있고 측정 가능한 시나리오 구성요소들이다. 
    - atomic block의 작은 크기는 합리적인 testing complexity를 제공하고, 여러개의 atomic block은 직렬적 또는 병렬적으로 연결되어 복잡한 시나리오를 만들어낸다. 
    - 종합적으로, 이 방법론은 edge accident scenario와 이와 유사한 scenario를 만들어내고, 시나리오의 수를 줄이며, coverage analysis를 제공한다.
  - 이 paper의 main contribution은 다음과 같다.
    - present atomic block : a modular and measurable scenario unit in logical abstraction level for AV validation
    - utilize accident report data in functional abstraction level to create atomic blocks in logical abstraction level and concrete scenarios in simulation
    - create evolving database of atomic blocks that can be combined to generate complex scenarios
    - implement AV assessment processes to identify potential edge scenarios for future iterations and mutations of atomic blocks and complex scenarios.
- 모르는 단어 
  - brevity : using only a few words or lasting only a short time
  - coverage analysis : In other words, coverage analysis is a method for quantifying the completeness of testing and helps identify any areas that may need additional testing or attention to ensure the safety and reliability of the autonomous vehicle.(by chatgpt)
