# Formalising Traffic Rules for Accountability of Autonomous Vehicles

## ABSTRACT

- 중요한 문장 :
  - To solve this issue, we view trafﬁc rules from legal texts as requirements for autonomous vehicles. 
  - If we can prove that an autonomous vehicle always satisﬁes these requirements during its operation, then it cannot be held responsible in a collision.

## INTRODUCTION

- 중요한 문장 : 
  - However, another important but rarely studied area is the liability aspect of autonomous vehicles. That is, when a collision occurs, we want to determine who is responsible for it. >> From an engineering perspective, we address this issue by ensuring that autonomous vehicles always comply with the trafﬁc rules so that they cannot be held liable for a collision.
  - As the ﬁrst step to make the trafﬁc rules machine checkable, we propose to concretise and formalise trafﬁc rules.
  - Two major milestones for formalising law are the works of Sergot et al. [6] and Bench-Capon et al. [7]
  - We also decided not to use Deontic Logic because our goal is to elicit a set of formal speciﬁcation for autonomous vehicles from legal texts.
  - Another line of work other than formalisation of law which is related to our work is the formal veriﬁcation of autonomous vehicles.
  - In this work, we show that by concretising and formalising trafﬁc rules in Higher Order Logic using the Isabelle theorem prover, it is possible to check the compliance of trafﬁc rules unambiguously and formally.
    - We formalise hybrid traces which could be perceived as the abstraction of autonomous vehicles’ behaviours obtained from the data recorded on a black box (see e.g. [17]) in Isabelle/HOL (Sec. III)
    - We formalise a subset of trafﬁc rules from the Vienna Convention for Road Trafﬁc which applies to highway scenarios in Isabelle/HOL (Sec. III);
    - We show a pattern for deriving a procedure for each rule to verify whether a hybrid trace satisﬁes the rule correctly (Sec. IV)