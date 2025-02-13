# 개발상식
- 클린코드 & 리팩토링 & 시큐어코딩
- [애자일](#애자일) 
- TDD
- DDD
- MSA
- OOP
- [OOP의 5가지 설계 원칙](#oop의-5가지-설계-원칙)
- 함수형 프로그래밍
- DevOps
- 3rd Party
- Git , Github, Gitlab
- REST API
- Parameter vs Argument
- Sync vs Async
- XSS
- [도커와 쿠버네티스](#도커란)

<br>

# 애자일
## 애자일 이란?
* ‘Agile = 기민한, 날렵한’ 이란 뜻으로 좋은 것을 빠르게 취하고, 낭비 없게 만드는 다양한 방법론을 통칭해 일컫는 말

* 절차보다는 사람이 중심이 되어 **변화에 유연하고 신속하게 적응하며, 효율적인 시스템을 개발**하는 방법론

* **반복적/점증적인 짧은 개발주기, 위험도를 감소시키고 고객의 요구사항 수용의 민첩성이 강조**된 개발 방법론

<br>

## 애자일 방법론의 진행 과정
* 애자일 방법론은 **계획 → 설계(디자인) → 개발(발전) → 테스트 → 검토(피드백)** 순으로 반복적으로 진행됩니다. 계획을 세운 후 다음 단계까지 기다려서 절차대로 진행하는 워터폴 모델과 달리 먼저 진행 후 분석, 시험, 피드백을 통하여 개선하여 나가는 진행 모델입니다.

<br>
<p align="center">
<img src="https://user-images.githubusercontent.com/33649908/129449270-4b75d314-3c3d-447c-9a08-8e2b0413c9ed.jpeg" width="60%">
</p>

1. **계획 및 분석** : 고객과 사용자가 원하는 바를 파악하여 타당성을 조사하고 SW 기능과 제약조건을 정의하는 명세서 작성, 대상이 되는 문제 영역과 사용자가 원하는 task를 이해하는 단계
2. **설계(디자인)** : 기획의도에 맞는 설계 및 디자인 추가 및 수정하는 단계
3. **개발(발전)** : 설계단계에서 만들어진 설계서를 바탕으로 프로그램을 작성, 코딩, 디버깅, 단위/통합테스트 수행
4. **테스트** : 발생 가능한 실행 프로그램 오류를 발견, 수정하는 단계
5. **검토(피드백)** : 기획의도를 파악하고 시험결과와 기획의 따라 수정할 부분을 제시하는 단계

<br>

## 애자일 방법론의 특징
* 고객과 개발자의 **지속적인 소통**을 통하여 변화하는 요구사항을 신속하게 수용한다.
* 개발자 개인의 가치보다는 팀의 목적을 우선시하며 **고객의 의견을 가장 우선시**한다.
* **팀원들과의 주기적인 회의 및 제품 시현**을 통한 방지를 점검한다.
* 진행하면서 프로그램을 시행해보고 **고객으로부터 피드백**을 받는다.
* 내부 구조 형성을 통한 **비용절감**에 힘쓰는 동시에 **프로그램 품질 향상**을 위해 노력한다.

<br>

## 애자일 방법론의 장/단점
### 장점 👍
* **프로젝트 계획에 걸리는 시간을 최소화**할 수 있다.
* 점진적으로 테스트할 수 있어서 **버그를 쉽고 빠르게 발견할 수 있다.**
* 계획 혹은 기능에 대한 **수정과 변경에 유연**하다.
* 고객 요구사항에 대한 **즉각적인 피드백에 유연하며 프로토타입 모델을 빠르게 출시**할 수 있다.
* 빠듯한 기한의 프로젝트를 **빠르게 출시**할 수 있다.

### 단점 👎
* 확정되지 않은 계획 및 요구사항으로 인한 **반복적인 유지보수 작업이 많다.**
* 고객의 요구사항 및 계획이 크게 변경될 경우 모델이 무너질 수 있다.
* 개인이 아닌 팀이 중심이 되다 보니 **공통으로 해야 할 작업들이 많을 수 있다.** (회의, 로그 등)
* 반복적인 업무로 속도는 빠를 수 있으나 **미흡한 기능들에 대한 대처가 필요**하다.
* 확정되지 않은 계획으로 **개발 진행 시 이해하지 못하고 진행하는 부분이 많을 수 있다.**

<br>

## 애자일 방법론의 종류
### 익스트림 프로그래밍(Extreme Programming, XP)
* 문서를 강조하지 않고 테스트를 우선하는 개발 방식, **개발 초기부터 테스트를 병행**하는 개발 방법론
* 고객과 함께 **2주 정도의 반복개발**
* 의사소통, 피드백, 단순성, 용기, 존중 강조

<br>
<p align="center">
<img src="https://user-images.githubusercontent.com/33649908/129449766-b5ca72c9-b3e4-4bac-981e-ca2b7fd4755d.png" width="50%">
</p>

1. **유저스토리** : 사용자 요구사항 수집, 의사소통 도구
2. **구조적 스파이크** : 설계상,기술상  잠재적 위험을 탐지하기 위한 간단한 프로그램, 기술적인 문제를 줄이고 유저 스토리 기반 개발일정에 대한 신뢰도 상승
3. **릴리즈 계획** : 전체 프로젝트 배포계획 확립
4. **주기** : XP핵심, 상황에 따른 릴리즈 및 계획수정
5. **승인 테스트** : 릴리즈 전의 인수 테스트(블랙박스 테스트), 고객수행
6. **작은 릴리즈** : 주기의 마지막 단계, 빠른 피드백

<br>

### 스크럼(Scrum)
* 30일마다 동작 가능한 제품을 제공하는 **스플린트를 중심**, 팀을 중심으로 한 반복적이고 점진적인 개발 방법론
* **제품 백로그**를 바탕으로 기술적으로 분할되고 **재해석된 스프린트**를 통해 구현하는 개발 방법론
* XP는 변화수용, 스크럼은 **선감지 처리 관점**

<br>
<p align="center">
<img src="https://user-images.githubusercontent.com/33649908/129450311-cab3f342-1ac5-4d8e-a05c-c30624f7b5e0.png" width="70%">
</p>

#### 구성요소
* **Sprint** : 반복주기 (Iteration, 30days)
* **Product Backlog** : 제품의 요구사항 목록
* **Sprint Backlog** : 해당 Sprint기간에 수행해야하는 Task 목록
* **Daily Scrum Meeting** : 매일 15분 정도 짧게 진행하는 미팅 (계획, 실적, 위험 공유)
* **Review** : Sprint 완료 시 고객 검토, Feedback을 받아 다음 Product Backlog에 적용
* **Retrospective Meeting** : Scrum Team에서 운영중인 시험 리뷰 및 개선 미팅
* **Burn Down/Up Chart** : 하나의 스프린트에 대한 소멸/완성 그래프
 
#### 역할자
* **Product Owner** : 요구사항을 정의하고 Product Backlog 업데이트
* **Scrum Team** : Product Backlog 구현
* **Scrum Master** : 제 3자 입장에서 Product Owner와 Scrum Team이 Scrum방법론을 제대로 진행 할 수 있도록 지원

***따라서 Scrum을 적용하려면 조직의 역할/구성/감리/산출물 등 다양한 영역에서 변화를 주어야 함***

<br>

### KANBAN (칸반)
* **연속적 흐름 처리** 방식. **칸반 보드**로 시각화되고 각각 단계는 열로 표시

<br>
<p align="center">
<img src="https://user-images.githubusercontent.com/33649908/129450158-f00a677f-46d1-4d09-bb2b-52af95104dc2.png" width="70%">
</p>

#### 구성요소
* **Kanban Board** : 프로세스를 가진 Board와 스토리카드를 이용하여 업무 흐름제어
* **Process** : 실제 업무가 이루어지는 단계 및 업무 수행을 통한 산출물 작성
* **Work Queue** : 대기형렬, 개발 대기, 테스트 대기, 배포/릴리즈 대기 과정
* **Total Work Time (총 주기 시간)** : 총 작업의 수행시간, 개별 업무의 Cycle Time의 합으로 구성


<br>

# OOP의 5가지 설계 원칙

SOLID

- [SRP(단일 책임 원칙)](#srp)
- [OCP(개방 폐쇄 원칙)](#ocp)
- [LSP(리스코프 치환 원칙)](#lsp)
- [ISP(인터페이스 분리 원칙)](#isp)
- [DIP(의존관계 역전 원칙)](#dip)

디자인 패턴이 특별한 상황에서 발생하는 문제에대한 구체적인 솔루션이라면

객체지향 설계원칙은 좀 더 일반적인 상황에서 적용가능한 설계기준입니다.

객체지향의 5가지 원칙을 지키면 객체지향의 가장 큰 장점을 극대화 할 수 있습니다.

## SRP

단일 책임 원칙

"한 클래스는 하나의 책임만을 가져야한다"는 원칙입니다.

예를들면 커뮤니티 사이트에서 회원 정보를 관리할 때, 회원의 정보와 회원이 작성한 게시글에대한 정보까지 하나의 클래스에서 관리하면 게시글에대한 변경사항이 있을 때, 회원 클래스를 수정해야합니다.

이처럼 변경사항이 있을 때, 그 변경에대해서 그와 관련된 부분만 수정할 수 있도록 설계해야한다는 원칙이 단일 책임 원칙입니다.

단일 책임 원칙에서 가장 중요한 것은 각각의 클래스가 가지는 책임의 범위를 적절하게 잘 조절하는 것입니다.

## OCP

개방 폐쇄 원칙

"확장에는 열려있고 변경에는 닫혀있다."는 원칙입니다.

여기서 확장과 변경의 의미는 다음과 같습니다.

확장 - 기능을 변경하거나 확장하는 것을 의미

변경 - 확장된 기능을 사용하는 코드를 수정하는 것을 의미

다형성을 활용해서 인터페이스를 구현한 새로운 클래스를 만들고 거기에 새로운 기능을 구현해주는 방식입니다.

예를들면, 게시판에 업로드를 하는 부분에대한 기능의 확장이 있을 때, 업로드 기능을 사용하는 부분에서는 기존에 사용하던 방식을 그대로 사용할 수 있도록 하는 것을 의미합니다.

하지만, 구현 객체를 변경하려면 클라이언트 코드를 변경해야하기 때문에, 객체를 생성하고, 연관관계를 맺어주는 별도의 조립, 설정자가 필요합니다. 

→ 이 과정을 스프링이 대신 해줍니다^^

## LSP

리스코프 치환 원칙

"인터페이스를 구현한 구현체 즉, 하위 클래스는 인터페이스의 규약을 다 지켜야한다."는 원칙입니다.

인터페이스를 구현한 구현체의 신뢰성을 올리기위한 원칙으로 상위 타입의 객체를 하위 타입의 객체로 형변환 해도 정상적으로 작동할 수 있도록 하기 위해서 적용합니다.

## ISP

인터페이스 분리 원칙

"인터페이스의 기능을 적당한 크기로 나눠서 인터페이스를 더 명확하고 대체 가능성을 높여야한다"는 원칙입니다.

특정 클라이언트를 위한 인터페이스 여러 개가 범용 인터페이스 하나보다 더 좋다는 의미입니다.

예를 들면, 커뮤니티 사이트에서 북마크 기능을 개발할 때, 회원 북마크 기능과 게시글 북마크 기능을 개발을 할 때, 북마크 기능 전체에대한 범용 인터페이스보다는 회원 북마크용 인터페이스와 게시글 북마크용 인터페이스를 만들어두는게 좋습니다. 

## DIP

의존관계 역전 원칙

"추상화에 의존해야지, 구체화에 의존하면 안된다."라는 원칙입니다.

의존성 주입은 이 원칙을 따르는 방법 중 하나입니다. 

OCP와 연관이 있는 원칙입니다.

클라이언트 코드가 구현 클래스가 아닌 인터페이스를 바라보게해서, 인터페이스에서 어떤 구현 클래스를 사용할지 선택하게 하는 방식입니다.

이런 방식으로 개발해야하는 이유는 역할에 의존하지않고 구현에 해당하는 구현체에 의존하게되면 변경시에 불필요한 코드 수정이 많이 발생하기 때문입니다.

OCP와 마찬가지로 다형성만으로는 구현 객체를 변경할 때, 클라이언트 코드도 변경해야하기 때문에 DIP를 지키기 어렵습니다. 

→ 그래서 스프링이 필요합니다!

# 도커란?

도커는 **'컨테이너 기반의 오픈소스 가상화 플랫폼'**
- 도커로 컨테이너를 띄운다.
- 컨테이너란?<br>
  애플리케이션 & 애플리케이션을 구동하는 환경을 격리한 공간<br>
  컨테이너에 프로그램을 띄워서 돌린다고 생각하면 된다.<br>
  보통 마이크로 서비스로 사용된다.<br>
    - 거대한 어플리케이션을 기능별로 나누어 변경/조합이 가능하게 한 것
    - 컨테이너를 사용하면 하나의 큰 어플을 서비스 단위로 잘라 빠르게 배포 가능.
    - 그리고 각각 분리해서 쓰니 변경사항이 분리된 다른 기능들에 영향 미치지 않음.

<br>

**기존의 가상머신(VM)과 컨테이너의 차이점**
<p align="center">
<img src="https://user-images.githubusercontent.com/67310666/127528645-e66d5480-6ab2-4816-8e59-4030f489b077.png" width="90%">
</p>

- 기존의 가상머신(VM) 서버
    - Server -> Hypervisor -> 각각의 Guest OS가 설치된 VM 구동
    - 가상 머신의 모든 자원을 사용
- 컨테이너 서버 <br>
    - Server -> Host OS -> Docker Engine -> Container 올리기
    - CPU, RAM, Disk, Network와 같은 운영체제의 자원을 필요한 만큼 컨테이너에 할당
    - 효율적!! 배포가 빠름!! but 컨테이너 하나가 자원을 많이 사용하면 장애 발생.
- 도커가 가진 컨테이너는 독립적이고 동적이다.
    - if, 당신의 app이 인기가 많아지면 그 컨테이너의 수를 늘리고, 다시 트래픽이 줄면 해당 컨테이너 수를 줄이면 된다. 
    - 즉, 도커 덕분에 매번 새로운 서비스를 만들 때마다 새로운 서비스를 사고, 설정할 필요가 없음
    - 하나의 같은 서버에 각기 다른 환경의 컨테이너를 설정할 수 있고, 이 컨테이너들은 각각 분리, 독립되어 있는 것이기 때문에 더욱 효율적
    <br>

```
쉽게 말하자면!
가상 컴퓨팅은 한 물리적 컴퓨터 안에 각각 OS를 가동하는 가상 컴퓨터들이 물리적 자원을 분할해서 쓰기 때문에 성능에 한계가 있음!
도커는 OS단까지 내려가는게 아니라 실행 환경만 독립적으로 돌리는 거라서 컴퓨터에 직접 요소들을 설치한거랑 별 차이 없는 성능을 낼 수 있음!
```
<br>

Youtube ["도커가 뭐고 왜 쓰는건가요?"](https://youtu.be/tPjpcsgxgWc)

<br>

# 쿠버네티스란?
<p align="center">
<img src="https://user-images.githubusercontent.com/67310666/128356721-8d8fc51a-eaf7-42b8-be50-5bbecd205523.png" width="50%">
</p>

쿠퍼네티스는 **'컨테이너 오케스트레이션 툴'**
- 오케스트레이션이란?<br>
컨테이너 수가 많아지면 관리와 운영에 있어 어려움이 있음. <br>
이러한 다수의 컨테이너 실행을 관리 및 조율하는 시스템.
오케스트레이션 엔진을 통해 컨테이너의 생성과 소멸, 시작 및 중단 시점 제어, 스케줄링, 로드 밸런싱, 클러스터링 등 컨테이너로 어플리케이션을 구성하는 모든 과정을 관리할 수 있음.

