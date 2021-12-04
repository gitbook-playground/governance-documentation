---
description: 사용자 거래 보상 프로그램 개요

---

# 거래 보상

25%\(`250,000,000 DYDX`\)는 지불된 수수료와 미결제 약정을 기반으로 프로토콜 상에서 거래하는 사용자에게 배포될 것입니다.

**목표**

* dYdX 레이어 2 퍼페추얼을 사용하도록 모든 트레이더 장려
* 시장 유동성 및 전반적인 상품 사용 가속화

## **개요**

![](../.gitbook/assets/image%20%283%29.png)

DYDX는 dYdX Layer 2 프로토콜에 대한 유료 및 미결제 이자의 조합을 보상으로 제공하는 공식을 기반으로 하여 트레이더에게 배포될 것입니다. DYDX는 5년 동안 28일 순환을 기준으로 배포될 예정이며 모든 베스팅 또는 락업에서 제외됩니다. 3,835,616 DYDX가 순환당 배포됩니다.

콥-더글라스 함수는 각 에폭 동안 각 트레이더에게 지급되는 DYDX의 양을 계산하는 데 사용됩니다.

$$ w\ =\ \left(\frac{f}{F}\right)^{\alpha } \times \ \left(\frac{d}{D}\right)^{1-\alpha } $$

$$ r=R\times \frac{w}{\sum\limits _{n} w_{n}} \ \ ,n=1,2...k $$

| 기간 | 정의 |
| :--- | :--- |
| r | 특정 트레이더에 대한 보상 |
| R | 에폭 동안 풀에 있는 모든 트레이더 간에 분할될 총 보상 |
| f | 이 에폭에서 트레이더가 지불하는 총 수수료입니다. |
| 주 | 개별 트레이더 점수입니다. |
| $${\sum\limits &lt;g id="1" ctype="italic" equiv-text="_"&gt;{n} w</g>{n}}$$ | 모든 트레이더 점수의 합계입니다. |
| F | 이 에폭의 모든 트레이더가 지불한 총 수수료입니다. |
| 일 | 이 에폭 내 모든 시장에 트레이더가 보유한 총 가중 미결제 약정\(시간당 측정\) |
| 일 | 이 에폭 내 모든 시장의 총 가중 미결제 약정\(시간당 측정\) |
| k | 이 에폭 내 총 트레이더 수 |
| α | 미결제 약정 대비 수수료의 가중치를 결정하는 범위 내 상수입니다. 처음에는 α=0.7입니다. |

다음 예는 위에 나열된 공식을 사용하여 트레이더 A, B 및 C가 획득한 거래 보상을 설명합니다.

![](https://lh4.googleusercontent.com/LWYcMg6ImkQCV1aVsS2jVwjcFfTmBG4u7JZHrnf4l4MmHcxCZlu_af57UaSgHhr6TYi9thIyr8794SECk6_E8Vn4sR2QJFniUSbQGhIZZrkvTf0QRHmzzvt6awR9N8kxHhCooRp4)

## FAQ

### 거래 보상을 받을 수 있는 자격은 무엇입니까?

dYdX 레이어 2 퍼페추얼의 모든 트레이더는 거래 보상으로 DYDX를 받을 자격이 있습니다.

이 상품은 dYdX의 [이용 약관](https://dydx.exchange/terms)에 정의된 대로 미국 또는 제한 지역의 트레이더에게는 제공되지 않습니다.

### 거래 보상 프로그램에서 DYDX가 얼마나 적립되었습니까?

주어진 에폭에서 사용자는 지불한 수수료, 평균 미결제 약정 및 예상 거래 보상을 여기에서 볼 수 있습니다.

### 거래 보상을 어떻게 청구할 수 있습니까? 제가 획득한 DYDX를 언제 인출하고 이체할 수 있습니까?

거래 보상을 통해 획득한 DYDX 토큰은 각 에포폭이 종료될 때 이체할 수 있습니다. DYDX 보유자가 토큰을 클레임하려면 에폭이 종료되고 약 `7일`\**(대기 기간**\)을 기다려야 합니다. 토큰이 클레임되면 사용하거나 dYdX 거버넌스에 위임할 수 있습니다.

트레이더는 [여기](https://dydx.community/dashboard)에서 모든 에폭이 종료될 때 거래 보상을 클레임할 수 있습니다.

사용자는 DYDX를 클레임하려면 "클레임"을 클릭하고 거래에 서명하고 가스 수수료를 지불해야 합니다.

![](../.gitbook/assets/image%20%284%29.png)

### 미결제 약정은 무엇입니까?

미결제 약정은 자산으로 정산되지 않은 미결제 퍼페추얼 계약의 총 수입니다. 미결제 약정은 매수 또는 매도된 계약의 총 수와 같으며 둘의 합계가 아닙니다. 미결제 약정이 증가하면 시장에 신규 또는 추가 자금이 유입되고 미결제 약정이 감소하면 시장에서 자금이 유출됩니다.

다음은 트레이더 A, B, C, D, E의 옵션 시장 거래 활동 표입니다. 미결제 약정은 매일의 거래 활동에 따라 USDC로 계산됩니다.

| 시간 | 거래 활동 | 미결제 약정\(USDC\) |
| :--- | :--- | :--- |
| 7월 1일 | **트레이더 A**는 1 BTC를 $30,000에 구입하고 **트레이더 B**는 1 BTC를 $30,000에 판매합니다. | $30,000 |
| 7월 3일 | **트레이더 C**는 5 BTC를 $30,000에 구입하고 **트레이더 D**는 5개의 BTC를 $30,000에 판매합니다. | $180,000 |
| 7월 5일 | **트레이더 A**는 1 BTC를 $30,000에 판매하고 **트레이더 D**는 1 BTC를 $30,000에 구입합니다. | $150,000 |
| 7월 10일 | **트레이더 E**는 5 BTC를 $30,000에 구입하고 **트레이더 C**는 5 BTC를 $30,000에 판매합니다. | $150,000 |

거래 보상 공식의 맥락에서, 미결제 약정은 모든 시장의 전반에 걸쳐 시간당 측정되며, 주어진 에폭 전반에 걸친 가중 평균은 보상 계산을 위해 사용됩니다.

### dYdX의 수수료 표가 무엇입니까?

dYdX는 거래 수수료를 결정할 때 메이커-테이커 수수료 모델을 사용합니다. dYdX에는 메이커(Maker)와 테이커(Taker) 등 두 가지 종류의 주문이 있습니다.

* 메이커 주문은 즉시 체결되지 않고 호가창에 남아있는 주문입니다. 이 주문들은 호가창에 깊이와 유동성을 더해줍니다.
* 반면 테이커 주문은 기존 메이커 주문을 즉시 삭제합니다. 테이커 주문은 호가창에서 유동성을 제거합니다.

메이커 및 테이커 수수료는 30일 거래량 가중 수수료 표를 사용하여 결정됩니다. 표준 수수료 표는 [여기](https://help.dydx.exchange/en/articles/4798040-perpetual-trade-fees)를 참조하십시오. DYDX 보유자는 DYDX의 현재 보유량에 따라 [거래 수수료 할인](trading-rewards.md)을 받을 수 있습니다.
