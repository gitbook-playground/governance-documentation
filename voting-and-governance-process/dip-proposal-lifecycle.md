---
description: dYdX 개선 제안 수명주기 개요

---

# DIP 제안 수명주기

## **제안 단계**

dYdX 거버넌스 프로세스는 \[gov.dydx.community\]의 거버넌스 포럼을 기반으로 하며, dYdX 개선 제안\(이하 'DIP'\)을 통해 승인됩니다.

아래의 초안에서는 거버넌스 개념의 시작 및 정의부터 실제 구현에 이르기까지 dYdX 거버넌스 프로세스가 어떻게 진행될 것인지를 설명합니다.
 해당 프로세스는 DYDX 커뮤니티의 피드백에 따라 변경될 수 있습니다.


다음 플로우 차트는 제안 통과를 위한 초기 제안 단계입니다.


![](../.gitbook/assets/dip-governance-process.png)

## 0\) 포럼 논의

누구나 커먼웰스 거버넌스 포럼\[gov.dydx.community\]에 호스팅되는 dYdX 거버넌스 포럼에 가입하고 모든 주제로 스레드를 만들 수 있습니다.
 커뮤니티 회원은 이메일 주소 또는 이더리움 지갑을 사용하여 등록해야 합니다.

## 1\) 오프체인 dYdX 의견 요청 제안\(DRC\) 생성

오프체인 dYdX 의견 요청\(DRC\) 생성은 거버넌스 개선 프로세스의 첫 번째 단계입니다.
 누구나 거버넌스 포럼\[dydx.community\]에 참여하여 오프체인 DRC를 생성하고 개선점을 논의할 수 있습니다.

DRC를 생성하려면 Github에서 이용 가능한 다음 템플릿을 사용하십시오.


DRC는 최소한 다음을 포함해야 합니다.


* DRC에 대한 짧고 간결한 제목

* 제안에 대한 짧고 간결한 설명

* DRC의 합리적인 근거(예: 제안 이유)

* 포럼 게시물의 제목은 'DRC: DRC에 대한 짧은 제목'을 포함해야 합니다.
    예) DRC: 새로운 시장 요청
* 커뮤니티 회원이 오프체인 개선점 투표에 사용할 수 있는 커뮤니티 여론조사


## 2\) 오프체인 DRC 논의 / 피드백 기간

거버넌스 포럼에 글이 게시되면 DRC의 향후 개선을 위해 모든 질문과 의견에 답변을 달고 고려 대상에 포함해야 합니다.

## 3\) 스냅샷 오프체인 여론조사

오프체인 DRC가 대략적인 합의에 도달하면 `10,000 DYDX` 이상을 보유한 커뮤니티 회원은 스냅샷에서 DRC에 대해 오프체인 투표를 생성할 수 있습니다\([https://snapshot.org/\#/dydx/create](https://snapshot.org/#/dydx/create)\).

스냅샷은 사용자가 오프체인으로 견해를 표명할 수 있는 간단한 투표 인터페이스입니다.
 스냅샷 상의 투표에는 투표에 사용된 주소에 위임된 DYDX 수에 따라 가중치가 부여됩니다.


DRC 제출자는 DRC에 대한 세부 정보, 투표 시스템, 투표 시작일 및 종료일, 스냅샷 블록 번호를 제공해야 합니다.
 스냅샷 블록 번호는 투표에 참여할 수 있는 커뮤니티 회원 상태를 제한합니다.
 스냅샷 블록 번호 이전에 토큰을 보유한 토큰 보유자가 투표에 참여할 수 있습니다.


스냅샷 투표 기간은 `5일` 로 설정해야 합니다.

제안 및 투표는 서명된 메시지일 뿐이며, IPFS에 저장되며 커먼웰스 포털을 통해 이용할 수 있습니다.


## 4\) DIP 온체인 생성

대략적 합의에 도달하면 해당 유형의 제안에 대해 충분한 제안권을 보유한 커뮤니티 회원이 온체인 DIP를 제출할 수 있습니다.
 온체인 DIP는 스마트 컨트랙트 호출을 통해 시작됩니다.
 해당 제안은 스냅샷 상 오프체인 DIP 투표의 개표 결과에 기반해야 하며, 하나 또는 여러 개의 활동(제안당 최대 10개)으로 구성될 수 있습니다.


DIP를 생성하려면 계정에 요구되는 최소 보유/위임 토큰 수를 충족해야 합니다.
 제안 생성 시 타임락 실행자를 명시해야 합니다.
 초기 파라미터는 다음과 같이 설정됩니다\(거버넌스에 의해 수정될 수 있음\).

| 매개 변수 | 설명 | 단기 타임락 실행자 | 머클-파서 실행자 | 장기 타임락 실행자 | 스타크웨어 실행자 |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 제안 임계점 | 제안 생성을 위해 보유/위임된 최소 토큰 | 총 공급의 0.5% | 총 공급의 0.5% | 총 공급의 2% | 총 공급의 0.5% |

## 5\) DIP 온체인 투표

온체인 DIP가 생성되면, 해당 제안은 **현재** `6570` 블록 또는 약 1일\(블록당 13초 가정\)에 해당하는 투표 딜레이로 정의되는 기간 동안 `보류` 상태에 진입합니다. 즉, DIP의 생성 1일 뒤 사용자 스냅샷이 촬영되며, 이때 해당 제안이 `활성` 상태로 전환됩니다.

투표 딜레이 후에 투표 기간이 활성화됩니다. 투표 기간의 길이는 제안 유형에 따라 다릅니다.


다음에서 DIP 상태 플로우 차트를 확인할 수 있습니다.


![](../.gitbook/assets/dip-lifecycle.png)

DIP가 온체인으로 생성되면, 해당 DIP에는 **투표 딜레이**, **투표 기간**, **최소 정족수** 및 최소 **투표 격차**가 적용됩니다. 초기 파라미터는 다음과 같이 설정됩니다\(거버넌스에 의해 수정될 수 있음\).

| 매개 변수 | 설명 | 단기 타임락 DIP | 머클-파서 DIP | 장기 타임락 DIP | Starkware DIP |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 투표 딜레이 |  | 6,570블록 | 6,570블록 | 6,570블록 | 6,570블록 |
| 투표 기간 |  | 4일 | 2일 | 10일 | 7일 |
| 최소 정족수 | DIP 제안 통과에 필요한 찬성표 최소 수 | 총 공급의 2% | 총 공급의 1% | 총 공급의 10% | 총 공급의 2% |
| 투표 격차 | DIP 제안 통과에 필요한 찬반 격차 | 총 공급의 0.5% | 총 공급의 0.5% | 총 공급의 10% | 총 공급의 0.5% |

## 6\) 제안 대기열 진입 및 실행

DIP가 통과되면 어떤 주소든 대기열 진입 방법을 호출하여 해당 제안을 타임락 대기열로 이동시킬 수 있습니다. DIP가 통과된 경우에만 대기열에 진입할 수 있습니다.

| 매개 변수 | 설명 | 단기 타임락 실행자 | 머클-파서 실행자 | 장기 타임락 실행자 | 스타크웨어 실행자 |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 타임락 지연 | 제안이 통과되고 대기열에 진입한 후 실행되기 전에 발생하는 딜레이 | 2일 | 0일 | 7일 | 2일 |
| 실행 그레이스 기간 | 투표 후 제안을 실행할 수 있는 기간 | 7일 | 7일 | 7일 | 7일 |
| 최소 타임락 지연 | 제안이 실행되기 전 발생하는 최소 딜레이\(대기열 진입 후\) | 1일 | 0일 | 5일 | 1일 |
| 최대 타임락 지연 | 제안이 실행되기 전 발생하는 최대 딜레이\(대기열 진입 후\) | 7일 | 1일 | 21일 | 7일 |

## 8\) \(선택 사항\) 제안 취소

DIP 수명주기 동안 제안자는 언제든지 DIP를 취소할 수 있습니다. 새로운 DIP가 제출되면 동일한 수명주기가 적용됩니다.



## 자주 묻는 질문

### 투표 딜레이의 목적은 무엇입니까?

**투표 딜레이**는 제안 제출 후 제안에 대한 투표가 시작되기 전에 기다려야 하는 이더라움 블록 수입니다.

DYDX 투표권은 제안 제출 전 또는 제안에 대한 **투표 딜레이** 기간 동안 한 주소에 전적으로 위임되어야 합니다.

현 시점에서 **투표 딜레이**은 약 1일에 해당하는 `6,570 블록`으로 설정됩니다. 이 값은 제안 생성 시점의 현재 블록 번호에 추가됩니다.


향후 dYdX 거버넌스는 **투표 딜레이** 기간의 연장 또는 축소를 위해 투표할 수 있습니다. **투표 딜레이** 연장에는 명백한 이점이 있습니다. 하지만 기회주의적인 엣지 사례 악용과 같은 잠재적인 부작용을 초래할 수도 있습니다.


### 제안 임계값의 목적은 무엇입니까?

DYDX는 자유롭게 거래할 수 있는 자산이므로, 누구나 시장 거래를 통해 거버넌스 참여를 시도할 수 있습니다. 그러나 기만적인 투표를 강제로 통과시키려면 단기 타임락의 경우 최소 500만 DYDX, 장기 타임락의 경우 2000만 DYDX가 필요합니다.
 이를 달성한다 하더라도 이 금액은 매우 비싸며, 가격 변동을 고려할 때 공격을 통해 얻을 수 있는 순이익보다 더 많은 비용이 들 것입니다.


한 그룹이 어떻게든 악의적인 인수를 달성하더라도 타임락 딜레이를 통해 영향을 받은 에이전트는 프로토콜에서 자산을 인출할 시간을 확보할 수 있습니다. 이는 프로토콜을 포킹할 수 있는 기회이기도 합니다. 나머지 선의 행위자들은 이 방법을 선택할 가능성이 높습니다.

###
