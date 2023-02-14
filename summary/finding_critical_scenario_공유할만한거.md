# Finding Critical Scenarios for Automated Driving Systems : A Systematic Mapping Study 중 critical scenario에 대한 내용

## 정리

- critical scenario와 비슷한 의미를 가진 단어들 : edge cases, corner cases

- corner case는 normal operational parameter와 희귀하고 비정상적인 condition의 조합이다. 일상적이지 않고 특이한 condition들의 특별한 조합을 가진 corner case들이 edge case이다.

- critical scenario는 시스템의 design, safety analysis, verification or validation에 사용될 수 있는, 잠재적인 위험요소를 가진 scenario이다.

![figure_5](../image/finding_critical_scenarios_figure5.png)

- fig. 5에 적혀있듯이, 알려지지 않은 critical scenario는 unknown triggering condition에서 나오거나 unknown safety-critical operation situation에서 나올 수 있다.

- unknown critical scenario는 unknown scenario factor로 이루어지거나 unknown combination of known scenario factors로 이루어질 수 있다.

- 이를 종합하면, Critical Scenario Identification 방법은 triggering condition, safety-critical operational situation, 아니면 앞의 둘의 조합 중 피해를 입힐 수 있는 것을 찾는 것이다.

## 사용된 용어

- triggering condition : Specific conditions of a scenario that serve as an initiator for a subsequent system reaction, possibly leading to a hazardous behavior.

- Safety-Critical Operational Situation : Traffic conditions(within the ODD), where hazard is very likely to propagate to a harm.

## 이번 연구에서 생각해볼만한 점

- critical scenario가 어떻게 구성되는지를 알면 critical scenario를 분류하는 기준을 만드는데 도움이 됨.
