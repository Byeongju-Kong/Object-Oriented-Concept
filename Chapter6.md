# 객체 지도

### 기능을 중심으로 구조를 종속시키는 방법은 범용적이지 않고 재사용이 불가능, 변경이 취약

ex) 출발지에서 목적지까지 가는 길을 사람에게 물었을 때, 사람은 구두로 대답하기 때문에, 텍스트처럼 다시 볼 수 없고 현재의 요구만을 만족시킨다, 나중에 대답을 다시 생각하면서 찾아가야하고, 출발지-목적지에 대한 정보만 알 수있다.

✔️ **해결 방법 지향적인 접근법**

### 구조를 중심으로 기능을 종속시키는 접근법은 범용적, 재사용 가능, 변경에 유연하게 대처

ex) 출발지에서 목적지까지 가는 길을 위해 지도를 얻었을 때, 찾아가는 도중 지도를 다시 볼 수 있고, 후에 출발지와 목적지가 변경되어도 다시 사용할 수 있다. 

✔️ **구조적이고 문제 지향적인 접근법**

### ✔️기능 기반으로 모델을 구축하면 범용적이지 않고 재사용이 불가능하며 변경에 취약하다

### ✔️구조 기반으로 모델을 구축하는 편이 더 범용적이고 이해하기 쉬우며 변경에 안정적이다

---

# 기능 설계 vs 구조 설계

### 기능 측면의 설계

- 제품이 사용자를 위해 **무엇을 할 수 있는지**에 초점
- 훌륭한 기능은 대가를 지불하고서라도 구매할 수 있을 정도로 매력적이어야한다. 따라서, 소프트웨어 개발 **초기에**는 **사용자가 원하는 것과 그것을 위해 시스템이 제공해야하는 기능에 초점을 맞춰야한다.**
- 훌륭한 기능은 훌륭한 소프트웨어의 **충분조건**

### 구조 측면의 설계

- 제품의 **형태가 어떠해야하는지**에 초점
- 사용자들이 내부를 볼 수 없지만, 사용자의 변하는 요구사항을 반영할 수 있도록 **쉽게 확장 가능한 소프트웨어를 창조해야한다**.
- 훌륭한 구조는 훌륭한 소프트웨어의 **필요조건**

### ✔️ 사용자들의 요구는 계속 변하기 때문에, 사용자들이 원하는 기능을 지속적으로 제공할 필요가 있지만, 변화하는 요구사항에 유연하게 대처하려면 안정적인 구조가 필수적이다.

우리는 미래를 예측할 수 없다. 단지 대비할 수 있을 뿐이다.

→ 미래에 대비하는 최선책은 예측이 아닌 변경을 수용할 수 있는 선택의 여지를 설계에 마련해놓는 것이다.

**→ 설계를 하는 목적은 나중에 설계하는 것을 허용하는 것**

### ✔️ 객체지향에서는 자주 변경되지 않는 안정적인 객체 구조를 바탕으로 시스템 기능을 객체 간의 책임으로 분배

### ✔️ 객체지향에서는 객체의 구조에 집중하고 기능이 객체의 구조를 따르게 만든다.

→ **기능이 변경되더라도 객체 간의 구조는 그대로 유지**된다.

---

# 두가지 재료 : 기능과 구조

객체지향 세계를 구축하기 위해서는 사용자에게 제공할 **'기능'**과 기능을 담을 안정적인 **'구조'**가 필요하다.

### 기능

사용자가 자신의 목표를 달성하기 위해 사용할 수 있는 시스템의 서비스

### 구조

시스템의 기능을 구현하기 위한 기반으로, 기능 변경을 수용할 수 있도록 안정적이어야한다.

## 기능과 구조에 관한 두가지 기법

### ✔️ 구조는 사용자나 이해관계자들이 도메인(domain)에 관해 생각하는 개념과 개념들 간의 관계로 표현한다.

### ✔️ 기능은 사용자의 목표를 만족시키기 위해 책임을 수행하는 시스템의 행위로 표현한다.

### 유스케이스 모델링 : 기능을 수집하고 표현하기 위한 기법

결과물 : 유스케이스

### 도메인 모델링 : 구조를 수집하고 표현하기 위한 기법

결과물 : 도메인 모델

---

# 안정적인 재료 : 구조

### ✔️ 모든 소프트웨어는 사용자의 필요성을 충족시키기 위해 존재

→ 소프트웨어 사용자는 자신이 관심을 가지고 있는 특정 분야의 문제를 해결하기 위해 소프트웨어 사용

## 도메인 모델

### 도메인 : 사용자가 프로그램을 사용하는 대상 분야

ex) 은행 종사자는 은행 도메인을 고객과 계좌 사이의 돈의 흐름으로, 게임 플레이어들은 게임 도메인을 캐릭터와 몬스터, 그리고 몬스터가 떨어뜨리는 아이템 간의 관계로 파악

### 모델 : 대상을 선택적으로 단순화하고 의식적으로 구조화한 형태

→ 다뤄야하는 중요한 문제에만 집중할 수 있도록 필요한 지식만 재구성한 것

### ✔️ 도메인 모델이란, 소프트웨어가 목적하는 영역 내의 개념과 개념 간의 관계, 다양한 규칙이나 제약 등을 주의 깊게 추상화한 것

→ 소프트웨어 개발과 관련된 이해관계자들이 도메인에 대해 생각하는 관점

### ✔️ 도메인 모델은 단순히 다이어그램이 아닌 이해관계자들이 바라보는 멘탈 모델이다.

멘탈 모델이란, 사람들이 자기 자신, 다른 사람, 환경, 자신이 상호작용하는 사물들에 대해 갖는 모형

→ 소프트웨어 사용자들 역시 도메인에 존재하는 현상을 이해하고 현상에 반응하기 위해 도메인과 관련된 멘탈 모델을 형성

### ✔️제품을 설계할 때 제품에 관한 모든 것이 제품에 대해 가지고 있는 사용자들의 멘탈 모델과 정확히 일치해야 한다

→ 사람들은 제품이 **자신의 멘탈 모델과 유사한 방식으로 제품이 반응하고 움직일 것이라고 기대하기 때문**에 훌륭한 디자인이란 사용자가 예상하는 방식에 따라 정확하게 반응하는 제품을 만드는 것

### 멘탈 모델의 세가지 구분

1. 사용자 모델
→ 사용자가 제품에 대해 가지고 있는 개념들의 모습
2. 디자인 모델
→ 설계자가 마음 속에 갖고 있는 시스템에 대한 개념화
3. 시스템 이미지
→ 최종 제품

### → 디자인 모델을 기반으로 만든 시스템 이미지가 사용자 모델을 정확하게 반영하도록 노력해야 한다. ( 시스템 이미지는 사용자의 관점을 반영해야 한다 )

## 도메인의 모습을 담을 수 있는 객체지향

### 소프트웨어에서도 최종 제품은 사용자의 관점을 반영해야 한다

→ 애플리케이션이 도메인 모델을 기반으로 설계돼야 한다는 것을 의미하고
**객체 지향은 위의 요구 사항을 가장 범용적으로 만족시킬 수 있는 거의 유일한 모델링 패러다임이다**

### ✔️ 객체지향을 사용하면 사용자들이 이해하고 있는 도메인의 구조와 최대한 유사하게 코드를 구조화 할 수 있다.

 객체 지향은 사람들이 만지고 느끼고 볼 수 있는 실체를 시스템 안의 객체로 재창조한다.

→ 동적인 객체의 복잡성을 정적인 타입을 이용해 단순한 타입으로 만들 수 있으며, 클래스라는 도구를 이용해 타입을 코드 안으로 옮길 수 있다.

### → **사용자의 관점, 설계자의 관점, 코드의 모습을 모두 유사한 형태로 유지할 수 있다.
     이를 연결완전성 ( 표현적 차이 )라고 한다.**

## 표현적 차이

소프트웨어 객체는 현실 객체를 은유하여 재창조하기 때문에, 현실 객체가 가진 특성을 가지지 않을 수 있고 갖고 있지 않은 특성을 가질 수도 있다.
→ **소프트웨어 객체는 현실 객체를 왜곡하더라도, 현실 객체의 특성을 토대로 구축된다**.

### ✔️ 소프트웨어 객체와 현실 객체 사이의 의미적 거리를 표현적 차이(의미적 차이)라 한다

→ 은유를 통해 현실 객체와 소프트웨어 객체 사이의 **차이를 최대한 줄이는 것이 핵심**

하지만 대부분의 우리가 개발하는 서비스들이나 게임은 현실에 존재하지 않는 가상의 세계를 대상으로 한다
ex) 현실에 존재하지 않는 게임 속 괴물들과 마법, 현실 세계에는 존재하지 않은 새로운 유형의 웹 서비스

→ **가상의 세계를 창조하는 작업에서 현실 객체를 은유할 수가 없다.**

### ✔️ 따라서, 사용자가 도메인에 대해 생각하는 개념을 은유를 통해 투영해야한다.

소프트웨어 객체는 은유하려는 대상이 현실적인지, 현실적인지 않은지에 상관 없이 **도메인 모델을 통해 표현되는 도메인 객체들을 은유해야한다.**

**→ 도메인 모델을 기반으로 설계하고 구현하면 사용자의 멘탈 모델을 설계에 반영할 수 있다.**

### ✔️ 표현적 차이는 소프트웨어를 이해하고 수정하기 쉽게 만들어주기 때문에 중요하다.

→ **코드의 구조가 도메인의 구조를 반영**하기 때문에 도메인을 이해하면 코드를 이해하기가 훨씬 수월하다

### 계좌 ( 도메인 모델 )

- 계좌번호
- 예금액

### Account ( 구현 )

- account Number
- amount

## 불안정한 기능을 담는 안정적인 도메인 모델

### ✔️ 도메인 모델의 핵심은 사용자가 도메인을 바라보는 관점을 반영해 소프트웨어를 설계하는 것

→ 사용자가 도메인을 바라보는 관점을 반영하는 이유는 **사용자들이 누구보다 도메인의 본질적인 측면을 잘 이해하고 있기 때문이다.** 사용자들이 ****도메인을 구성하는 개념과 개념 간의 관계를 가장 잘 알고 있다.

여기서 본질적이라는 것은, **변경이 적고 비교적 그 특성이 오랜 시간 유지된다는 것**을 의미한다.

### ✔️ 사용자가 도메인 모델을 기반으로 설계하면 안정적인 구조를 제공할 수 있다.

소프트웨어의 가장 큰 적은 항상 발생하는 변경이다. 변경은 사용자의 요구에 의해서 이루어지는데, **처음부터 사용자가 도메인을 바라보는 관점으로 설계를 하고 코드를 작성한다면 기능의 변경에 안정적으로 대처할 수 있다.**

---

# 불안정한 재료 : 기능

## 유스케이스

### ✔️ 유스케이스란, 사용자가 시스템을 통해 사용자의 목표를 달성하기 위해 사용자와 시스템 간에 이뤄지는 상호작용의 흐름을 텍스트로 정리한 것

✔️기능적 요구사항 : 시스템이 사용자에게 제공해야 하는 기능의 목록을 정리한 것

### 엘리스터 코오번의 유스케이스에 대한 설명

> 유스케이스는 시스템의 **이해관계자들 간의 계약을 행위 중심으로 파악**한다. 유스케이스는 이해관계자들 중 일차 액터(Primary Actor)라 불리는 **행위자의 요청에 대한 시스템의 응답**으로, 다양한 조건 하에 있는 시스템의 행위를 서술한다. **일차 액터는 어떤 목표를 달성하기 위해 시스템과의 상호작용**을 시작한다. 시스템은 모든 이해관계자들의 요구에 응답하고 이해관계를 보호해야 한다. **특별한 요청과 관계되는 조건에 따라 서로 다른 일련의 행위 혹은 시나리오가 전개**될 수 있다. 유스케이스는 이렇게 서로 다른 시나리오를 묶어준다. [Cockburn 2000]

💡일차액터(Primary Actor)란, **시스템의 서비스 중에 하나를 요청하는 이해관계자**로, 하나의 목표를 가지고 유스케이스를 시작하는 액터를 의미. 일반적으로 **시스템과 연동하는 외부 시스템 역시 일차 액터의 범주**에 포함시킨다. ( 외부 시스템이 어떤 시스템에게 요청을 보낸다면, 어떤 시스템의 관점에서 외부시스템 역시 일차액터라는 말으로 해석된다. )

### ✔️ 유스케이스의 가치는 사용자들의 목표를 중심으로 시스템의 기능적인인 요구사항들을 이야기 형식으로 묶을 수 있다는 것

→ 산발적으로 흩어져 있는 기능에 **사용자 목표라는 문맥**을 제공함으로써, **각 기능이 유기적인 관계를 지닌 체계를 이룰수 있게** 한다. ( 여러 가지 기능을 하는 시스템에서, 사용자의 목표를 위한 기능들을 뽑아 유기적으로 연결한다고 해석된다. )

> 사용자 목표가 유스케이스의 핵심이다. 유스케이스는 공통의 사용자 목표를 통해 강하게 연관된 시나리오 집합니다. [ Fowler 2003 ]

## 유스케이스의 특성

### 1. 유스케이스는 사용자와 시스템 간의 상호작용을 보여주는 텍스트다.

 유스케이스는 다이어그램이 아닌, 텍스트이다. 중요한 것은 유스케이스 안에 포함돼 있는 **상호작용의 흐름**이다.
**핵심은 사용자와 시스템 간의 상호작용을 일련의 이야기 흐름으로 표현**하는 것이다. 

### 2. 유스케이스는 하나의 시나리오가 아니라 여러 시나리오들의 집합이다.

✔️ 시나리오란, 유스케이스를 통해 **시스템을 사용하는 하나의 특정한 이야기 또는 경로 (유스케이스 인스턴스)**

 사용자가 어떤 목적을 위해 시스템을 사용하는데, **시스템이 사용자의 목적을 위해 제공해야 하는 많은 기능들을 몇 개의 시나리오로 구성**할 수 있다.

### 3. 유스케이스는 단순한 피처 목록과는 다르다.

✔️ 피처란, 시스템이 수행해야 하는 기능의 목록을 단순하게 나열한 것. **피처들은 유기적이지 않고 독립적인 개념**

 이런 피처들을 유기적으로 묶고, 사용자와의 상호작용 흐름 속에서 두 치퍼를 포함하는 이야기를 제공함으로써, 시스템의 기능에 대해 의사소통을 할 수 있는 문맥을 얻을 수 있는 것이 유스케이프이다.

→ **유스케이스는 단순한 기능의 나열이 아닌, 이야기를 통해 연관된 기능들을 함께 묶는 것**이다. 

### 4. 유스케이스는 사용자 인터페이스와 관련된 세부 정보를 포함하지 말아야 한다.

 유스케이스는 자주 변경되는 사용자 인터페이스 요소는 배제하고 사용자 관점에서 시스템의 행위에 초첨을 맞춘다. 이처럼 사용자 인터페이스를 배제한 유스케이스 형식을 **본질적인 유스케이스**라 칭한다.

### 5. 유스케이스는 내부 설계와 관련된 정보를 포함하지 않는다.

 유스케이스의 목적은 내부 설계를 설명하는 것이 아닌, **연관된 시스템의 기능을 이야기 형식으로 모으는 것**이다.

 **유스케이스에서 객체 설계로의 전환은** 공학적인 규칙과 원칙을 기반으로 한 변환 작업이 아니라 **경험과 상식과 의사소통을 기반으로한 창조 작업**이다.

## 유스케이스는 설계 기법도, 객체지향 기법도 아니다

### ✔️ 유스케이스는 단지 사용자가 바라보는 시스템의 외부 관점만을 표현한다.

유스케이스는 단지 **사용자가 시스템을 통해 무엇을 얻을 수 있고, 어떻게 상호작용할 수 있느냐에 관한 정보만 기술**

### ✔️ 유스케이스는 단지 기능적 요구사항을 사용자의 목표라는 문맥을 중심으로 묶기 위한 것

 단지 **외부에 제공해야 하는 행위만을 포함**하기 때문에, 유스케이스에서 **내부 구조를 유추할 수 없다**. 또**한 객치지향과의 연관성이 없다**. 유스케이스는 객체지향이 아닌 다른 패러다임에서도 사용할 수 있고, 객체지향도 유스케이스가 아닌 방법으로 요구사항을 명시할 수 있다.

### ✔️ 유스케이스는 객체의 구조나 책임에 대한 어떤 정보도 제공하지 않는다.

 유스케이스에선 단순 외부에 제공하는 행위만을 알 수 있다. 다만, 유스케이스의 설명에서 도메인 모델에서 사용할 용어에 대한 힌트정도를 얻을 수 있다( ex : 은행에 대한 유스케이스에서 '이자', '계좌' 등등 ). 하지만 이들은 약간의 힌트 밖에 되지 않는다.

---

# 재료 합치기 : 기능과 구조의 통합

## 도메인 모델, 유스케이스, 그리고 책임-주도 설계

 객체지향은 모든 것이 객체라는 사상에서 출발한다. 따라서 **시스템은** 사용자의 목표를 만족시키기 위해 **사용자와 협력을 하는 크고 자율적인 객체**이다. **사용자에게 제공하는 기능은 시스템의 책임**이라고 볼 수 있고, 이 **책임은 여러 객체들의 수많은 책임들로 나뉘어**진다.

### ✔️ 유스케이스는 사용자에게 제공할 기능을 시스템의 책임으로 보게 함으로써, 객체 간의 안정적인 구조에 책임을 분배할 수 있는 출발점을 제공한다.

 유스케이스에는 사용자와의 상호작용의 흐름이 있고, 사용자에게 제공해야 할 기능들이 있다. 이 기능들을 시스템의 책임으로 보게 하고, 시스템의 책임들은 더 작은 책임들로 나뉘어진다.

### ✔️ 도메인 모델을 기능을 수용하기 위해 은유할 수 있는 안정적인 구조를 제공한다.

 나뉘어진 작은 책임들을 도메인 모델을 기반으로 적절한 객체에 할당한다.

### ✔️ 책임-주도 설계 방법은 시스템의 기능을 역할과 책임을 수행하는 객체들의 협력 관계로 바라보게 함으로써 유스케이스와 도메인 모델을 통합한다.

 유스케이스를 통해 책임들을 나누고, 도메인을 통해 적절한 객체에 책임을 할당함으로써, 책임-주도 설계 방법이 이루어진다. 

 물론, 책임-주도 설계를 위해 반드시 유스케이스와 도메인 모델이 필요한 것은 아니다. 중요한 것은 사용자의 관점에서 시스템의 기능을 명시하고, 사용자와 설계자가 공유하는 안정적인 구조를 기반으로 기능을 책임으로 변환하는 체계절차를 따라야 한다는 것인데, 좋은 방법이 유스케이스와 도메인 모델이기 때문에 많은 사람들이 사용하는 것으로 생각된다.

## 기능 변경을 흡수하는 안정적인 구조

### 도메인 모델이 안정적인 이유

1. 도메인 모델을 구성하는 개념은 **비즈니스가 없어지거나 완전히 개편되지 않는 한 안정적으로 유지**된다.
ex ) 정기예금을 관리하는 도메인에서 정기예금과, 계좌, 이자율, 이자란 개념은 정기예금이라는 금융상품이 없어지거나 완전히 개편되지 않는 한 안정적으로 유지되는 개념이다.
2. 도메닝 모델을 구성하는 **개념 간의 관계는 비즈니스 규칙을 기반으로** 하기 때문에 **비즈니스 정책이 크게 변경되지 않는 한 안정적으로 유지**된다. 
ex) 정기예금 도메인에서 이자는 정기예금이 만기가 되거나 중도 해지를 하는 경우에 한해서 단 한번 지급된다. 따라서 계좌와 이자 간의 관계는 이와 같은 핵심적인 비즈니스 규칙이 변경되지 않는 한 동일하다.

### **기능적인 요구사항이 변경**될 경우 **책임과 객체간의 대응관계만 변경하면 된다.**

→ 변경에 대한 파급효과를 최소화하고 요구사항 변경에 유연하게 대응할 수 있는 시스템 구축 가능

### ✔️ 객체지향에서 가장 큰 장점은 도메인을 모델링하기 위한 기법과 도메인을 프로그래밍하기 위한 기법이 동일하다는 점

→ 도메인 모델링에서 사용한 객체와 개념을 부드럽게 프로그래밍 설계에서의 객체와 클래스로 변환가능
→ **연결완전성**

### ✔️객체지향에서 연결완정성의 역방향 역시 성립한다( 코드의 변경으로부터 도메인 모델의 변경 사항을 유추할 수 있다 )

→ 도메인 모델과 코드가 동일한 모델링 패러다임을 공유하기 때문에 **코드의 수정 = 모델의 수정**
→ **가역성 (reversibility)**

### 💡 안정적인 도메인 모델을 기반으로 시스템의 기능을 구현하라. 도메인 모델과 코드를 밀접하게 연관시키기 위해 노력하라
→ 유지보수하기 쉽고 유연한 객체지향 시스템을 만드는 첫걸음