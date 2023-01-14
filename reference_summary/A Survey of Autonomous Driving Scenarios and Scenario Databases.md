# A Survey of Autonomous Driving Scenarios and Scenario Databases

[PDF](/reference_summary/A_Survey_of_Autonomous_Driving_Scenarios_and_Scenario_Databases.pdf)

keywords : autonomous driving scenarios, scenario dataset, scenario database, scenario description

1. Abstract : <br>*this paper sumarizes the research progress of autonomous driving scenarios and scenario databases*
  - 모르는 단어
    - comprehensive : complete and including everything that is necessary
    - connotation : something suggested by an object or situation
    - perspective : a particular way of considering something.
2. Introduction 
  - 요약 : <br> 이번 페이퍼는 다음과 같은 관점으로 autonomous driving scenario와 scenario databases를 정리했다. (autonomous driving scenario / scenario description standard / scenario dataset / scenario database / summary and prospect)
  - 모르는 단어
    - criterion : a standard by which you judge, decide about, or deal with something.
    - significance : importance
3. SCENARIO IN AUTONOMOUS DRIVING
  - A. Scenario Definition 요약 : <br> *scenario describes the external roads, traffic facilities, weather and traffic participants as well as the driving tasks and states of the vehicle itself. It is an organic combination and comprehensive reflection of the driving environment, traffic participants and driving behavior within a certain time and space, and it will change dynamically.*
  - B. Scenario Elements and Layered Model 요약 : <br> *Scenario is a combination of various scenario elements in a certain time and space, and there is a strong coupling relationship between them*
    - divide by perspective of autonomous driving test requirements : environmental elements, traffic participant elements, self-vehicle tasks
    - divide by basic attributes of scenario elements : static elements, dynamic elements
    - divide by topological relationship of scenario elements : road elements, traffic participant elements, meteorological elements, network elements
    - six - layer model by PEGASUS project <br> L1 Road layer : Road topology, pavement quality, pavement boundaries, etc <br> L2 Traffic infrastructure layer : Structural boundaries, traffic signs, signal lights, etc <br> L3 Temporary manipulation layer of L1 and L2 : Temporary facilities on roads, such as temporary road closures, road construction sites, etc <br> L4 Objects layer : Traffic participants, and the status, behavior, etc. of traffic participants <br> L5 : Environment layer : Weather, electromagnetic strength, temperature, etc. <br> L6 Data communication layer : V2X information, digital map information, etc.
  - 모르는 단어
    - premise : an idea or theory on which a statement or action is based
    - omit : to fail to include or do something
    - temporal : relating to practical matters or physical things, rather than spiritual ones.
    - manoeuvre : a movement or set of movements needing skill and care
    - comprehensive : complete and including everything that is necessary
    - dimensionality : the quality of having or appearing to have height, length, and width rather than being flat
    - extent : the degree or limit of something
    - connotation : a feeling or idea that is suggested by a particular word although it need not be a part of the word's meaning, or something suggested by an boject or situation
    - pavement : sidewalk
    - constrain : to control and limit something
    - V2X : 자동차가 다른 모든것과 연결하는 기술
    - constitute : to be or be considered as something
    - meteorological : relating to weather conditions
    - topological : 위상적으로???
4. SCENARION DESCRIPTION STANDARD
  - A. ASAM OpenX Standards 요약 : <br> ![figure](/image/survey_autonomous_figure1.png) <br> *In ASAM OpenX, OpenSCENARIO describes dynamic content, OpenDRIVE describes the road network for static content, and OpenCRG describes the road network for static content. The three standards complement each other and cover both static and dynamic aspects of autonomous vehicle simulation applications.*
  - B. OpenDRIVE 요약 : <br> 
  - C. OpenSCENARIO 요약 : <br>
  - 모르는 단어
    - calibration : the units of measurement marked on an instrument so that it can measure accurately
    - parsing : to examine computer data and change it into a form that can be easily read or understood