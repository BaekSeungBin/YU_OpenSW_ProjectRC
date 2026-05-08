# 🎮 Project RC: Roguelike Card Game

<img width="1024" height="1024" alt="Image" src="https://github.com/user-attachments/assets/5b0cfe01-29e8-40df-abd5-1e6c1b58648a" />

A turn-based roguelike card game built with Unity.

**Student**: 22421647 백승빈  
**Email**: tmdqls0203sd@naver.com  
**GitHub Repository**: (https://github.com/BaekSeungBin/YU_OpenSW_ProjectRC)

---

# ConCeptualization Phase


## 📑 Contents

- [1. Business Purpose](#-1-business-purpose)
- [2. System Context](#-2-system-context)
- [3. Use Case List](#-3-use-case-list)
- [4. Concept of Operation](#-4-concept-of-operation)
- [5. Problem Statement](#-5-problem-statement)
- [6. Glossary](#-6-glossary)
- [7. References](#-7-references)

---

## 📌 1. Business Purpose

### 🔹 Project Background / Motivation

최근 게임을 플레이하면서 화려한 그래픽과 음악, 방대한 맵을 특징으로 하는 고사양 게임(AAA 게임)뿐만 아니라, 비교적 단순한 구조를 가지면서도 전략적인 재미를 제공하는 인디 게임이나 로그라이크 장르에도 관심을 가지게 되었다.  

특히 카드 게임 기반의 턴제 로그라이크 게임을 플레이하며 매 판마다 다른 전략을 요구하는 점에서 큰 흥미를 느꼈고, 이러한 게임을 직접 제작해보고자 본 프로젝트를 기획하게 되었다.  

이러한 장르는 **랜덤 요소를 통해 매 플레이마다 다른 경험을 제공하며, 높은 재플레이성**을 가진다.  

본 프로젝트에서는 이러한 장르적 특성을 바탕으로 **턴제 전투와 카드 시스템을 결합한 게임**을 개발하는 것을 목표로 한다.

---

### 🎯 Goal

- 턴제 전투 시스템 구현  
- 카드 기반 스킬 시스템 구현  
- 랜덤 요소를 포함한 로그라이크 구조 설계  
- 전략적인 플레이가 가능한 게임 구현  

---

### 👤 Target Market

- 전략 게임을 선호하는 사용자  
- 카드 게임 및 로그라이크 장르를 즐기는 사용자  

---

## 📌 2. System Context
<img width="879" height="1177" alt="Image" src="https://github.com/user-attachments/assets/a7cf8018-d9cc-46d2-8a4a-f54b873c1597" />

### 🧩 구성 요소

- **Player**: 카드 선택, 턴 종료 등 입력을 통해 게임과 상호작용  
- **Game System (Unity)**: 전체 게임 로직 처리  
- **Battle System**: 턴제 전투 처리  
- **Card System**: 카드 관리 및 효과 적용  
- **Enemy AI**: 적 행동 제어  
- **Relic System**: 패시브 효과 적용  
- **Stage System**: 스테이지 진행 관리  
- **Display**: 게임 상태를 화면에 출력  

---

## 📌 3. Use Case List

| No | Use Case | Actor | Description |
|----|----------|-------|------------|
| 1 | Game Start | Player | 게임 시작 |
| 2 | Use Card | Player | 카드 사용 |
| 3 | End Turn | Player | 턴 종료 |
| 4 | Enemy Action | System | 적 자동 행동 |
| 5 | Boss Battle | System | 보스 전투 |
| 6 | Battle End | System | 전투 종료 |
| 7 | Select Reward | Player | 카드 또는 유물 선택 |
| 8 | Move Stage | Player | 다음 스테이지 이동 |
| 9 | Game Over | System | 플레이어 사망 시 종료 |

---

## 📌 4. Concept of Operation

### ▶ Game Start
- **Purpose**: 게임 시작  
- **Approach**: Start 버튼 선택 시 초기 상태 생성  
- **Dynamics**: 게임 시작 시  
- **Goals**: 시작 기능 구현  

### ▶ Use Card
- **Purpose**: 카드 사용  
- **Approach**: 카드 선택 후 코스트 확인 및 효과 적용  
- **Dynamics**: 플레이어 턴  
- **Goals**: 카드 사용 기능  

### ▶ End Turn
- **Purpose**: 턴 종료  
- **Approach**: 버튼 클릭 시 적 턴 전환  
- **Dynamics**: 턴 종료 시  
- **Goals**: 턴 전환  

### ▶ Enemy Action
- **Purpose**: 적 행동  
- **Approach**: AI 기반 행동 수행  
- **Dynamics**: 플레이어 턴 종료 후  
- **Goals**: 적 행동 구현  

### ▶ Boss Battle
- **Purpose**: 보스 전투  
- **Approach**: 보스 등장 및 전투  
- **Dynamics**: 보스 방 진입  
- **Goals**: 최종 전투 구현
  
### ▶ Battle End
- **Purpose**: 전투 종료  
- **Approach**: HP 0 시 종료  
- **Dynamics**: 전투 중  
- **Goals**: 승패 판정  

### ▶ Select Reward
- **Purpose**: 보상 선택  
- **Approach**: 카드 또는 유물 선택  
- **Dynamics**: 전투 승리 후  
- **Goals**: 보상 시스템 구현  

### ▶ Move Stage
- **Purpose**: 스테이지 이동  
- **Approach**: 다음 방 선택  
- **Dynamics**: 전투 종료 후  
- **Goals**: 스테이지 진행
  
### ▶ Game Over
- **Purpose**: 게임 종료  
- **Approach**: 플레이어 HP 0 시 종료  
- **Dynamics**: 전투 중  
- **Goals**: 게임 종료 처리  

---

## 📌 5. Problem Statement

### ⚠ 예상 문제

- 카드와 유물 간 밸런스 문제  
- 랜덤 요소로 인한 난이도 편차  
- 턴제 상태 관리 복잡성  
- UI와 로직 연동 문제  
- 플레이어 선택에 따른 흐름 관리  

---

### ⚙ NFRs

- Unity 기반 개발  
- 안정적인 게임 실행  
- 직관적인 UI 제공  
- 빠른 응답 속도  
- 성능 최적화  

---

## 📌 6. Glossary

- **Card**: 행동 단위  
- **Relic**: 패시브 아이템  
- **Turn**: 행동 단위  
- **Roguelike**: 반복 플레이 장르  
- **Energy**: 카드 사용 자원  

---

## 📌 7. References

- Unity Documentation  
- Roguelike Game Design  
- Card Game Mechanics  
- Game Programming Patterns  

---

## 🛠 Tech Stack

- Unity  
- C#  

---

## 🎮 Gameplay (Optional)

![Gameplay](./assets/gameplay.png)


# Analysis Phase

# Analysis

## Project RC : Roguelike Card Game

- **Student ID**: 22421647  
- **Author**: 백승빈  
- **Email**: tmdqls0203sd@naver.com  

---

# Revision History

| Revision Date | Version | Description | Author |
|---|---|---|---|
| 2026-05-08 | 0.2 | Revised Analysis Document | 백승빈 |

---

# Contents

1. Introduction  
2. Use Case Analysis  
3. Domain Analysis  
4. User Interface Prototype  
5. Glossary  
6. References  

---

# 1. Introduction

## 1.1 Summary

본 문서는 Unity 기반 턴제 로그라이크 카드 게임 **"Project RC"** 에 대한 Analysis 보고서이다.  
본 문서에서는 게임 시스템의 Use Case 분석, Domain 분석 및 User Interface Prototype을 설명한다.

---

## 1.2 Introduce "Project RC"

최근 인디 게임 시장에서는 전략성과 높은 재플레이성을 제공하는 로그라이크 장르가 큰 인기를 얻고 있다.  
특히 카드 기반 턴제 로그라이크 게임은 플레이어가 상황에 따라 다양한 전략을 선택할 수 있다는 특징을 가진다.

**"Project RC"** 는 카드 시스템과 격자(Grid) 기반 턴제 전투를 결합한 로그라이크 게임이다.  
플레이어는 맵 위에서 이동 카드를 사용하여 위치를 조정하고, 근접 공격 또는 원거리 공격 카드를 사용하여 적과 전투한다.

각 스테이지는 하나의 전투 맵으로 구성되며, 플레이어는 스테이지 내부의 잡몹과 보스를 상대해야 한다.  
보스를 처치하면 스테이지를 클리어할 수 있으며, 이후 카드 또는 유물(Relic) 보상을 획득하여 덱을 강화할 수 있다.

---

## 1.3 Goal

본 Analysis 보고서의 주요 목표는 다음과 같다.

- 격자(Grid) 기반 턴제 전투 시스템 설계
- 카드 기반 행동 시스템 구현
- 로그라이크 요소가 포함된 성장 구조 설계
- 전략적인 위치 선정 및 전투 시스템 구현
- 객체 간 관계 및 시스템 흐름 분석

---

# 2. Use Case Analysis

## 2.1 Use Case Diagram
<img width="1421" height="1511" alt="Image" src="https://github.com/user-attachments/assets/7dddb696-0e4b-41a8-a926-c03ddb2cf39c" />

Player 관점에서 시스템이 제공하는 기능을 Use Case Diagram으로 표현하였다.

Game System은 내부적으로 다음과 같이 구성된다.

- Battle System
- Grid System
- Card System
- Enemy AI System
- Relic System

플레이어는 다음 행동을 수행할 수 있다.

- 이동
- 카드 사용
- 턴 종료
- 보상 선택

적 행동 및 전투 판정은 시스템이 자동으로 처리한다.

---

## 2.2 Use Case Description

# Use Case #1 : Game Start

## General Characteristics

| Item | Description |
|---|---|
| Summary | 플레이어가 게임을 시작할 때 필요한 기능 |
| Scope | Project RC |
| Level | User Level |
| Author | 백승빈 |
| Last Update | 2026-05-07 |
| Status | Analysis |
| Primary Actor | Player |
| Preconditions | 플레이어가 메인 메뉴 화면에 있어야 한다. |
| Trigger | 플레이어가 Start 버튼을 클릭할 때 |
| Success Post Condition | 게임이 초기 상태로 생성되고 첫 번째 스테이지가 시작된다. |
| Failed Post Condition | 게임이 시작되지 않고 메인 메뉴에 머문다. |

## Main Success Scenario

| Step | Action |
|---|---|
| 1 | 플레이어가 Start 버튼을 클릭한다. |
| 2 | 시스템은 플레이어의 기본 체력과 초기 덱을 생성한다. |
| 3 | 시스템은 시작 유물 선택 화면을 출력한다. |
| 4 | 첫 번째 스테이지를 로드한다. |
| 5 | 전투가 시작된다. |

## Extension Scenarios

| Step | Branching Action |
|---|---|
| 2 | 2a. 저장 데이터가 없는 경우 |
|  | ...2a1. 기본 초기값으로 게임을 시작한다. |

---

# Use Case #2 : Select Starting Relic

## General Characteristics

| Item | Description |
|---|---|
| Summary | 플레이어가 시작 유물을 선택하는 기능 |
| Scope | Project RC |
| Level | User Level |
| Author | 백승빈 |
| Last Update | 2026-05-07 |
| Status | Analysis |
| Primary Actor | Player |
| Preconditions | 게임이 시작된 상태여야 한다. |
| Trigger | 시작 유물 선택 화면이 표시될 때 |
| Success Post Condition | 선택한 유물이 플레이어에게 적용된다. |
| Failed Post Condition | 유물이 적용되지 않는다. |

## Main Success Scenario

| Step | Action |
|---|---|
| 1 | 시스템은 랜덤 유물 3개를 출력한다. |
| 2 | 플레이어가 유물 하나를 선택한다. |
| 3 | 시스템은 선택한 유물 효과를 플레이어에게 적용한다. |
| 4 | 전투를 시작한다. |

---

# Use Case #3 : Move

## General Characteristics

| Item | Description |
|---|---|
| Summary | 플레이어가 격자 맵에서 이동하는 기능 |
| Scope | Project RC |
| Level | User Level |
| Author | 백승빈 |
| Last Update | 2026-05-07 |
| Status | Analysis |
| Primary Actor | Player |
| Preconditions | 플레이어 턴이어야 한다. |
| Trigger | 플레이어가 이동 카드를 사용하거나 이동 입력을 수행할 때 |
| Success Post Condition | 플레이어가 새로운 칸으로 이동한다. |
| Failed Post Condition | 이동할 수 없는 위치일 경우 이동하지 않는다. |

## Main Success Scenario

| Step | Action |
|---|---|
| 1 | 플레이어가 이동 행동을 선택한다. |
| 2 | 시스템은 이동 가능한 칸을 표시한다. |
| 3 | 플레이어가 이동할 칸을 선택한다. |
| 4 | 플레이어가 해당 위치로 이동한다. |

## Extension Scenarios

| Step | Branching Action |
|---|---|
| 2 | 2a. 장애물 또는 적이 있는 경우 |
|  | ...2a1. 해당 위치로 이동할 수 없다. |

---

# Use Case #4 : Use Card

## General Characteristics

| Item | Description |
|---|---|
| Summary | 플레이어가 카드를 사용하여 효과를 발동하는 기능 |
| Scope | Project RC |
| Level | User Level |
| Author | 백승빈 |
| Last Update | 2026-05-07 |
| Status | Analysis |
| Primary Actor | Player |
| Preconditions | 플레이어 턴이어야 하며 카드가 핸드에 존재해야 한다. |
| Trigger | 플레이어가 카드를 선택할 때 |
| Success Post Condition | 카드 효과가 정상적으로 적용된다. |
| Failed Post Condition | 에너지가 부족하거나 대상이 존재하지 않는다. |

## Main Success Scenario

| Step | Action |
|---|---|
| 1 | 플레이어가 핸드에서 카드를 선택한다. |
| 2 | 시스템은 카드 코스트를 확인한다. |
| 3 | 카드 효과를 실행한다. |
| 4 | 에너지를 차감한다. |
| 5 | 사용된 카드를 버린다. |

## Extension Scenarios

| Step | Branching Action |
|---|---|
| 2 | 2a. 에너지가 부족한 경우 |
|  | ...2a1. 카드 사용을 취소한다. |
| 3 | 3a. 공격 범위 내 적이 없는 경우 |
|  | ...3a1. 카드 사용을 취소한다. |

---

# Use Case #5 : End Turn

## General Characteristics

| Item | Description |
|---|---|
| Summary | 플레이어 턴을 종료하고 적 턴으로 전환하는 기능 |
| Scope | Project RC |
| Level | User Level |
| Author | 백승빈 |
| Last Update | 2026-05-07 |
| Status | Analysis |
| Primary Actor | Player |
| Preconditions | 플레이어 턴이어야 한다. |
| Trigger | 플레이어가 End Turn 버튼을 클릭할 때 |
| Success Post Condition | 적 턴이 시작된다. |
| Failed Post Condition | 턴이 전환되지 않는다. |

## Main Success Scenario

| Step | Action |
|---|---|
| 1 | 플레이어가 End Turn 버튼을 클릭한다. |
| 2 | 시스템은 남은 카드를 정리한다. |
| 3 | 적 턴을 시작한다. |
| 4 | 적 행동 종료 후 플레이어 턴으로 전환한다. |

---

# Use Case #6 : Enemy Action

## General Characteristics

| Item | Description |
|---|---|
| Summary | 적 AI가 자동으로 행동하는 기능 |
| Scope | Project RC |
| Level | System Level |
| Author | 백승빈 |
| Last Update | 2026-05-07 |
| Status | Analysis |
| Primary Actor | System |
| Preconditions | 적 턴이어야 한다. |
| Trigger | 플레이어 턴 종료 |
| Success Post Condition | 적이 공격 또는 이동 행동을 수행한다. |
| Failed Post Condition | 적 행동이 수행되지 않는다. |

## Main Success Scenario

| Step | Action |
|---|---|
| 1 | 시스템은 플레이어와 적의 거리를 계산한다. |
| 2 | 공격 가능 거리일 경우 공격한다. |
| 3 | 공격할 수 없는 경우 플레이어 방향으로 이동한다. |
| 4 | 모든 적 행동 종료 후 플레이어 턴으로 전환한다. |

---

# Use Case #7 : Battle End

## General Characteristics

| Item | Description |
|---|---|
| Summary | 보스 처치 또는 플레이어 사망 시 전투를 종료하는 기능 |
| Scope | Project RC |
| Level | System Level |
| Author | 백승빈 |
| Last Update | 2026-05-07 |
| Status | Analysis |
| Primary Actor | System |
| Preconditions | 전투 중이어야 한다. |
| Trigger | 보스 또는 플레이어 HP가 0 이하가 될 때 |
| Success Post Condition | 전투 결과 화면이 출력된다. |
| Failed Post Condition | 전투가 종료되지 않는다. |

## Main Success Scenario

| Step | Action |
|---|---|
| 1 | 시스템은 보스의 HP 상태를 확인한다. |
| 2 | 보스가 사망했을 경우 스테이지 클리어를 실행한다. |
| 3 | 보상 선택 화면으로 이동한다. |

## Extension Scenarios

| Step | Branching Action |
|---|---|
| 1 | 1a. 플레이어 HP가 0 이하인 경우 |
|  | ...1a1. Game Over를 실행한다. |

---

# Use Case #8 : Select Reward

## General Characteristics

| Item | Description |
|---|---|
| Summary | 전투 보상을 선택하는 기능 |
| Scope | Project RC |
| Level | User Level |
| Author | 백승빈 |
| Last Update | 2026-05-07 |
| Status | Analysis |
| Primary Actor | Player |
| Preconditions | 전투에서 승리해야 한다. |
| Trigger | 보상 화면 출력 |
| Success Post Condition | 카드 또는 유물이 추가된다. |
| Failed Post Condition | 보상이 추가되지 않는다. |

## Main Success Scenario

| Step | Action |
|---|---|
| 1 | 시스템은 랜덤 카드 또는 유물을 출력한다. |
| 2 | 플레이어가 보상을 선택한다. |
| 3 | 선택한 보상이 적용된다. |
| 4 | 다음 스테이지가 시작된다. |

---

# Use Case #9 : Game Over

## General Characteristics

| Item | Description |
|---|---|
| Summary | 플레이어 사망 시 게임을 종료하는 기능 |
| Scope | Project RC |
| Level | System Level |
| Author | 백승빈 |
| Last Update | 2026-05-07 |
| Status | Analysis |
| Primary Actor | System |
| Preconditions | 플레이어 HP가 0 이하이어야 한다. |
| Trigger | 플레이어 사망 |
| Success Post Condition | Game Over 화면이 출력된다. |
| Failed Post Condition | 게임 종료 처리가 되지 않는다. |

## Main Success Scenario

| Step | Action |
|---|---|
| 1 | 시스템은 플레이어를 비활성화한다. |
| 2 | Game Over 화면을 출력한다. |
| 3 | 플레이어는 Retry 또는 Main Menu를 선택할 수 있다. |

---

# 3. Domain Analysis

## 3.1 GameManager

게임 전체 진행 흐름을 관리하는 클래스이다.

- 게임 시작
- 스테이지 전환
- 게임 오버 처리

---

## 3.2 BattleManager

턴제 전투 흐름을 관리하는 클래스이다.

- 현재 턴 관리
- 전투 종료 여부 관리
- 적 행동 순서 관리

---

## 3.3 GridManager

격자(Grid) 기반 맵을 관리하는 클래스이다.

- 플레이어 위치 관리
- 적 위치 관리
- 이동 가능한 칸 관리

---

## 3.4 CardManager

플레이어의 다음 정보를 관리하는 클래스이다.

- 덱(Deck)
- 핸드(Hand)
- 버리기 더미(Discard Pile)

---

## 3.5 Card

카드 정보를 저장하는 클래스이다.

### 포함 정보

- 카드 이름
- 에너지 코스트
- 공격력
- 사거리
- 카드 타입

---

## 3.6 RelicManager

플레이어가 보유한 유물을 관리하는 클래스이다.

---

## 3.7 Relic

유물 정보를 저장하는 클래스이다.

### 포함 정보

- 유물 이름
- 설명
- 패시브 효과

---

## 3.8 Player

플레이어 상태를 관리하는 클래스이다.

### 포함 정보

- HP
- Energy
- Position
- Deck
- Relic

---

## 3.9 Enemy

적 정보를 저장하는 클래스이다.

### 포함 정보

- HP
- Position
- Attack Damage
- Enemy Type

---

## 3.10 EnemyAI

적의 행동을 결정하는 클래스이다.

플레이어와의 거리 및 현재 상태에 따라 이동 또는 공격을 수행한다.

---

## 3.11 RewardManager

전투 종료 후 카드 또는 유물 보상을 생성하는 클래스이다.

---

## 3.12 UIManager

게임 내 UI를 관리하는 클래스이다.

### 표시 정보

- HP
- Energy
- Hand Card
- Enemy HP
- Turn Information

---

# 4. User Interface Prototype

## 4.1 Main Menu Screen

게임 실행 시 표시되는 화면이다.

### 구성 요소

- START 버튼
- CONTINUE 버튼
- EXIT 버튼
- 게임 로고

<img width="1953" height="1219" alt="Image" src="https://github.com/user-attachments/assets/924c3bf9-36a6-4d8c-973e-93f45af2e491" />


---

## 4.2 Relic Selection Screen

게임 시작 시 플레이어가 시작 유물을 선택하는 화면이다.

### 구성 요소

- 랜덤 유물 3개
- 유물 설명
- 선택 버튼

<img width="1536" height="1024" alt="Image" src="https://github.com/user-attachments/assets/41bf62fc-229e-4766-bb1a-f37bf8b69f9f" />

---

## 4.3 Battle Screen

게임의 핵심 전투 화면이다.

### 구성 요소

- 격자(Grid) 전투 맵
- 플레이어 위치
- 적 위치
- 플레이어 HP 및 Energy
- 카드 핸드 UI
- End Turn 버튼

<img width="1536" height="1024" alt="Image" src="https://github.com/user-attachments/assets/a72b800e-c5c9-4176-aac7-79dfaecdf9c1" />


## 4.4 Card Effect Screen

카드 사용 시 효과 애니메이션이 출력되는 화면이다.

### 구성 요소

- 데미지 숫자 표시
- 공격 이펙트
- 방어 증가 효과


---

## 4.5 Reward Screen

전투 승리 후 보상을 선택하는 화면이다.

### 구성 요소

- 카드 보상
- 유물 보상
- Skip 버튼

<img width="1536" height="1024" alt="Image" src="https://github.com/user-attachments/assets/f8c22702-bd9a-4fc6-98cb-a4bc8ff11017" />

---

## 4.6 Game Over Screen

플레이어가 사망했을 때 출력되는 화면이다.

### 구성 요소

- Game Over 텍스트
- Retry 버튼
- Main Menu 버튼

<img width="1536" height="1024" alt="Image" src="https://github.com/user-attachments/assets/18f374a3-bd8e-4901-8dd0-e7fc8c96607d" />


---

# 5. Glossary

| Term | Description |
|---|---|
| Grid | 플레이어와 적이 위치하는 격자형 맵 |
| Card | 플레이어가 사용하는 행동 카드 |
| Deck | 플레이어가 보유한 카드 목록 |
| Hand | 현재 사용 가능한 카드 목록 |
| Energy | 카드 사용 시 필요한 자원 |
| Relic | 패시브 효과를 제공하는 아이템 |
| Melee Attack | 인접한 적에게 사용하는 근접 공격 |
| Ranged Attack | 일정 거리 내 적을 공격하는 원거리 공격 |
| Turn | 플레이어 또는 적이 행동하는 순서 |
| Boss | 스테이지 클리어 조건이 되는 적 |
| Roguelike | 랜덤 요소와 반복 플레이를 특징으로 하는 장르 |

---

# 6. References

- Unity Documentation  
  https://docs.unity3d.com/

- Slay the Spire (MegaCrit, 2019)

- Into the Breach (Subset Games, 2018)

- Unity Asset Store  
  https://assetstore.unity.com/

- Game Programming Patterns  
  https://gameprogrammingpatterns.com/
