# 🎮 Lords of the Fallen - Soulslike RPG Clone

## 📌 프로젝트 개요

| 항목 | 내용 |
| --- | --- |
| 📅 **작업 기간** | 2024.10.04 ~ 2024.11.11 (약 1개월) |
| 🎮 **장르** | 소울라이크 3인칭 액션 RPG |
| 💻 **개발 언어** | Unreal Engine Blueprint |
| 🛠️ **개발 엔진** | Unreal Engine 5 |
| 👤 **참여 형태** | 개인 프로젝트 |

---

## 🧠 게임 소개

> **Unreal Engine을 활용한 'Lords of the Fallen' 스타일의 액션 RPG 모작 프로젝트**  
플레이어와 보스 간의 **실시간 전투와 패턴 전환**을 중심으로 설계된 개인 프로젝트입니다.  
**상태 기반 구조**, **공통 인터페이스**, **AI 거리/방향 판단**, **타겟팅 시스템** 등을 통해 몰입도 있는 전투 경험을 구현하였습니다.

- 전투는 **공격/피격/콤보 상태 전이**를 통해 유동적으로 구성되며, 열거형 기반 상태 정의로 명확한 조건 분기를 수행합니다.
- 무기 장착 및 공격 처리는 **무기 컴포넌트 + 인터페이스 기반 설계**를 통해 다양한 무기 유형을 일관된 방식으로 처리합니다.
- 적 AI는 Behavior Tree + Blackboard로 구성되며, **Service 노드를 활용한 실시간 거리/각도 감지**를 통해 전투 행동을 전환합니다.
- **Dot Product(내적)**을 활용하여 카메라 전방과 적의 방향 벡터를 비교하고, **가장 정면에 가까운 적을 타겟팅**합니다.
- 보스는 **1페이즈/2페이즈로 전환**되며, 원거리/근거리 스킬이 구분되어 다양한 전투 패턴을 연출합니다.

---

## 🧩 주요 기능

### 🧱 상태 기반 전투 시스템
- Idle, Combo, Evade, Hit, Dead 등 명확한 상태 분기
- 상태 변경 시 애니메이션 및 행동 제어 동기화
- 전투는 **공격/피격/콤보 상태 전이**를 통해 유동적으로 구성되며, 열거형 기반 상태 정의로 명확한 조건 분기 처리

### ⚔️ 무기 시스템 (컴포넌트 + 인터페이스 구조)
- 각 무기 액터는 공통 인터페이스를 상속해 장착/해제/공격 처리
- 컴포넌트 기반 설계로 재사용성과 확장성 확보
- **무기 장착 및 공격 처리를 통합된 방식으로 구조화**

### 🤖 적 AI 행동 전환 (BT + Blackboard + Service)
- 거리, 시야 방향, 상태에 따라 행동 전환 (추적, 공격, 대기)
- 페이즈 전환 시 몽타주, 사운드, 이펙트 동기화
- **Service 노드를 활용한 실시간 거리/각도 감지**
- 보스는 **1페이즈/2페이즈로 전환**, 근거리/원거리 스킬로 전투 패턴 차별화

### 🎯 타겟팅 시스템
- 카메라 전방 벡터와 적 방향 벡터를 Dot Product(내적)으로 비교
- **정면에 가장 가까운 적을 타겟팅**

---

## 🖼️ 게임 결과 화면

<table>
  <tr>
    <th>플레이어 콤보</th>
    <th>1페이즈 보스 근거리 공격</th>
  </tr>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/your-player-combo.gif" width="350px" height="200px"></td>
    <td><img src="https://github.com/user-attachments/assets/your-phase1-melee.gif" width="350px" height="200px"></td>
  </tr>
  <tr>
    <th>타겟팅 시스템</th>
    <th>2페이즈 원거리 스킬</th>
  </tr>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/your-targeting.gif" width="350px" height="200px"></td>
    <td><img src="https://github.com/user-attachments/assets/your-phase2-ranged.gif" width="350px" height="200px"></td>
  </tr>
</table>

<p align="center">※ 실제 플레이 중 캡처된 전투 연출 장면입니다.</p>

---

## 🔗 외부 링크

- 📹 [플레이 영상 보기](https://youtu.be/Na-bHM61pRQ)  
- 📄 [개발 명세서 (Notion)](https://melted-part-f0c.notion.site/Load-Of-Fallen-1dc924ed3149803bac73d3a4e054791f?pvs=4)  
- 💻 [GitHub 저장소](https://github.com/YEAHWA1010/Lords-of-the-Fallen)

---

## 📧 이메일

yea2979@naver.com
