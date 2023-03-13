# 새로운 주제조사

- 03/13까지 police report 논문을 읽은 후에 생각난 problem statement랑 연구 방법, diagram을 들고가야 한다

## 현재까지 내가 생각한 problem statement

- 어린이 보호구역에서 일어나는 사고들은 굉장히 치명적인 사고로 이어질 수 있다.(사족을 붙이자면 민식이 놀이 같이 어린이들이 오히려 법을 악용해 위험한 놀이를 하는 경우도 치명적인 사고에 포함할 수 있다.) 자율주행 자동차가 어린이 보호구역에서 일어날 수 있는 사고들에 대응하기 위해서는 이에 걸맞는 시나리오가 필요하다. 또한 이 시나리오에 자율주행 자동차가 대응할 수 있을지를 평가하는 기준 또한 필요하다.
  - 그래서 어떻게 할 것인가? 
    - 어린이 보호구역에서 일어났던 사고들, 일어날법한 사고들에서 요소들을 뽑아내고 분류한 다음 이를 이용해 재구성한 시나리오를 만든다.
      - 관련 논문 : 예전에 사고 시나리오에서 요소들을 분류한 다음 새로운 시나리오를 만드는 논문이 있었는데, 이를 참고해볼 수 있다.
    - 그 후 이 시나리오들을 정말 학습이 필요한 시나리오인지를 판단해서 고른다.
      - 이 방법은 이전 회의에서 지속적으로 이야기했었던 reward function이 될 수 있다.
    - 골라진 시나리오를 바탕으로 자율주행 자동차를 테스트 할 수 있는 환경을 구현한다.
      - 평가 지표 또한 하나의 function으로서 구성해볼 수 있다.
  - 근데 이거 이전까지 계속 이야기해보던 것이 아닌가?
    - 이전 회의에서는 솔직히 어떤게 문제가 되는지가 불분명해 너무 회의가 산으로 자꾸 갔었다. 방법론만 실컷 이야기하고 정작 해결해야 하는 문제가 정확히 나오지 않았다.
    - 이걸 생각할 때는 그래도 어떤 부분이 문제가 될지를 생각해봤다.(어린이 보호구역에서 일어나는 사고는 치명적이다.)

- 나라별로 다른 도로교통 법규들이 존재하는데(예를 들면 우회전 규정 등) 이에 따라 운전자가 안전운전을 하는 방법도 다르다. 현재 생성되는 시나리오들은 우리나라 법규 사정에 안 맞을수도 있다. 이를 보강하는 시나리오 생성이 필요하다.
  - 어떻게 생각해냈는가 : 
    - Police Report 논문과 같이 시나리오를 생성하는 방법 중에는 기존 데이터를 바탕으로 시나리오를 생성하는 방법이 있다.
    - 기존 데이터를 바탕으로 만들 시에는 기존 데이터가 생성된 나라에 맞는 시나리오가 생성될 것이다. 이런 시나리오들을 이용한 검증은 우리나라의 도로상황에 안맞을 수도 있다.
    - 다른 나라에서 생성된 시나리오 데이터셋이 우리나라 도로교통 법규에 맞는지 확인하는 절차 또한 필요하다.
      - 자율주행자동차가 도로교통법을 준수능력 취득에 대해 말하는 논문 : [PDF](../reference_summary/자율주행자동차에_대한_도로교통법_대응에_관한_소고-운전면허_규정을_중심으로.pdf)
    - 위의 어린이 보호구역 또한 다른 나라에 유사한 정책이 있을지라도 세부적인 법 적용은 우리나라 만의 정책이기 때문에 자율주행 자동차가 이에 적응하지 못 할수도 있다.
    - 위 사항들을 종합하면, 다른 나라에서 검증된 자율주행 알고리즘이여도, 우리나라 교통법규에 안 맞을수도 있다.
  - PROBLEM STATEMENT : 자율주행 자동차 알고리즘을 테스트하는 시나리오 중 우리나라 도로교통 법규에 맞춘 시나리오가 필요하다.
  - 연구방법 :
    - 우리나라 도로교통 법규 중 다른 나라들과 다른 법규를 찾는다. >> 만약에 이걸 주제로 삼으면 각 나라별 교통법규 차이를 자세히 조사하는 것이 필요하다.
      - 교통 법규에 관한 국제 협약이 있다는데, 우리나라 법규 중 국제 협약과 다른 점이 연구 대상이 될 수 있다.
        - Geneva Convention of Road Traffic : [PDF](../reference_summary/Geneva_Convention_of_Road_Traffic.pdf)
        - Vienna Convention of Road Traffic : [PDF](../reference_summary/Vienna_Convention_of_Road_Traffic.pdf)
    - 이 법규가 적용되는 상황을 시나리오를 구성하는 요소들로 분리한다.
      - 기존 데이터에서 요소를 분류해 새로운 시나리오를 만들어내는 논문이 있다. >> [관련 논문](../reference_summary/Generation_of_Modular_and_Measurable_Validation_Scenarios_for_Autonomous_Vehicles_Using_Accident_Data.pdf)
      - 도로교통법을 알고리즘으로 변환하기 위한 논리화, 도식화, 구조화를 다룬 논문 : [PDF](../reference_summary/자율주행자동차와_로봇윤리_그_법적_시사점.pdf) <br> 여기서 상당히 끝부분에 법들을 알고리즘화 할 필요성이 있다고 언급한다. 이 논문에서는 법을 알고리즘화 하는 방법론에 대해서는 이야기하지 않고 있다.
      - 현재 많은 혼란을 주고 있는 우회전 규정을 알고리즘 순서도로 구조화한 연구 : [PDF](../reference_summary/자율주행_시스템을_위한_우회전_구조화에_관한_연구.pdf)
        - 이 논문에서는 우회전 규정이라는 특정 법규를 이전 판례들을 바탕으로 중요한 요소를 뽑아내 알고리즘화 했고 순서도로 만들었다.
        - 시나리오 구성 요소를 뽑아내는데 참고할 만한 논문이다.
    - 그리고 이 요소들을 이용해 시나리오를 구성한다.
      - 이때, 교통법규를 가장 잘 드러내는 요소들을 찾아내고 강조하는 것이 중요하다. 
      - 또는 뒤에서 이야기되겠지만, 교통법규의 구성요소들을 수학적으로 모델링할 수도 있다.
      - 또는 법규 자체가 순서도 등으로 잘 구조화된 알고리즘 형태라면, 절차 자체를 자율주행 알고리즘이 시나리오를 잘 따르는가에 대한 평가 기준으로 삼을 수 있다.
      - 앞서 강조된 요소들은 다른 곳에서 만든 시나리오들이 우리나라 교통법규에 적합한지를 평가하는데 하나의 기준이 될 수 있다.
    - 시나리오가 만들어지면 이를 가상환경에서 구현하고 자율주행 알고리즘이 평가를 받을 수 있는 환경을 만들어 볼 수 있다.
      - 이는 이전 회의에서 지속적으로 이야기했던 부분이다. 
      - 다만 나는 시나리오를 이용해 이 체계를 만드는 구체적인 이유와 문제를 좀 더 붙인 거 같다.
  - 이전에는 이런 연구가 없었는가? (우리나라 연구 사례들)
    - 현재 많은 혼란을 주고 있는 우회전 규정을 알고리즘 순서도로 구조화한 연구 : [PDF](../reference_summary/자율주행_시스템을_위한_우회전_구조화에_관한_연구.pdf)
    - 자율주행 운전 능력 평가 시스템의 개발 방향과 내용을 제시한 논문 : [PDF](../reference_summary/Development_Direction_of_Autonomous_Vehicle_Driving_Ability_Evaluation_System_based_on_Virtual_Environment.pdf)
  - 과연 우리나라 교통 법규 증 특이한 것이 시나리오를 새로 평가해야 할 만큼의 이유가 있을까.
    - police report 논문 마지막에 추후 연구되어야 할 분야에서 "공식 교통 규정은 자동으로 검증 가능한 수식으로 형식화 될 수 있으며, 이는 더 많고 더 나은 테스트 오라클을 제공합니다."라고 제안했다.
      - 여기서 "oracle"은 다음과 같은 의미이다. : In the context of software testing, an oracle is a mechanism or principle used to determine whether a software system or its component behaves correctly or not. (chatGPT)
      - 이와 연관지어보면, 우리나라의 공식 교통 법규가 검증 가능한 수식으로 만들어지면, 자율주행 자동차 알고리즘을 테스트 하기 위한 더 많은 오라클이 생성된다고 볼 수 있다.
      - 이 주제는 특이한 우리나라의 법규를 검증 가능한 수식에서 더 나아가, 테스트할 수 있는 시나리오 데이터셋으로 만든다는 점에서 의미를 둘 수 있다.
      - 이 논문에서 이 주제와 관련된 논문을 인용했다. <br> Rizaldi, A., and Althoff, M. Formalising Traffic Rules for Accountability of Autonomous Vehicles. In Proceedings of the IEEE International Conference on Intelligent Transportation Systems (2015) [PDF](../reference_summary/Formalising_Traffic_Rules_for_Accountability_of_Autonomous_Vehicles.pdf)

## 이와 관련된 논문들 읽고 정리하는 공간

- police report : [PDF](../reference_summary_other_people/generating_effective_test_cases_for_self_driving_cars_from_police_reports.pdf) [SUMMARY](../summary/SUMMARY_generating_effective_test_cases_for_self_driving_cars_from_police_reports.md)
- 사고 시나리오로부터 구성요소들을 정의 및 분리 후 새로운 시나리오를 만들어내는 방법론 [PDF](../reference_summary/Generation_of_Modular_and_Measurable_Validation_Scenarios_for_Autonomous_Vehicles_Using_Accident_Data.pdf) [SUMMARY](../summary/Generation_of_modular_and_measurable_validation_scenarios_of_autonomous_vehicles_using_accident_data.md)
- 교통 법규를 자율주행 자동차에 적용시키고자 하는 논문 : [PDF](../reference_summary/Formalising_Traffic_Rules_for_Accountability_of_Autonomous_Vehicles.pdf) [SUMMARY](../summary/SUMMARY_Formalising_Traffic_Rules_for_Accountability_of_Autonomous_Vehicles.md)
- 현재 많은 혼란을 주고 있는 우회전 규정을 알고리즘 순서도로 구조화한 연구 : [PDF](../reference_summary/자율주행_시스템을_위한_우회전_구조화에_관한_연구.pdf) [SUMMARY](../summary/SUMMARY_Development_Direction_of_Autonomous_Vehicle_Driving_Ability_Evaluation_System_based_on_Virtual_Environment.md)
- 자율주행 운전 능력 평가 시스템의 개발 방향과 내용을 제시한 논문 : [PDF](../reference_summary/Development_Direction_of_Autonomous_Vehicle_Driving_Ability_Evaluation_System_based_on_Virtual_Environment.pdf) [SUMMARY](../summary/SUMMARY_자율주행_시스템을_위한_우회전_구조화에_관한_연구.md)
- 자율주행 운전 능력 평가 시스템의 개발 방향과 내용을 제시한 논문 : [PDF](../reference_summary/Development_Direction_of_Autonomous_Vehicle_Driving_Ability_Evaluation_System_based_on_Virtual_Environment.pdf)
- 