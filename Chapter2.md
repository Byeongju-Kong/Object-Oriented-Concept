# Chapter2

# 객체지향과 인지 능력

### 객체 지향이 직관적이고 이해하기 쉬운 패러다임인 이유

✔️ 인간은 선천적으로 눈에 보이는 세상을 자율적이고 독립적인 객체들로 분해할 수 있는 능력이 있기 때문
✔️ 또한 이를 넘어서 인간은 추상적인 사물들도 개념적으로 경계를 지을 수 있음

### → 따라서, 객체란 인간이 분명하게 인지하고 구별할 수 있는 물리적 or 개념적 경계를 지닌 
     어떤 것이다.

### → 객체 지향의 패러다임은 인간이 인지할 수 있는 다양한 객체들이 모여 현실 세계를 이루는 
     것처럼 소프트웨어의 세계 역시 인간이 인지할 수 있는 다양한 소프트웨어 객체들이 모여 
     이뤄진다는 믿음에서 출발한다.

---

# 객체

✔️ 하나의 개별 상태로 인지되는 것은 모두 다 객체가 될 수 있다.
✔️ 인간의 인지능력으로 다른 것과 구분할 수 있고, 생성 시점 등을 알 수 있다.

### → 이런 객체의 다양한 특성을 효과적으로 설명하기 위해서는 객체 상태, 행동 ,식별자를 지닌 실체로 보는 것이 가장 효과적이다

---

# 상태

### 왜 상태가 필요한가

✔️ 객체가 주변 환경과의 **상호작용에 어떻게 반응하는가**는 **그 시점까지 객체에 어떤 일이 발생했느냐에 따라 좌우**

✔️ 어떤 행동의 결과는 과거에 어떤 행동들이 일어났었느냐에 의존 ( **과거의 행동으로 인해 어떤 상태를 지니느냐** )

### 과거 행동의 결과들을 보고 현재 발생한 결과를 판단하는 복잡함 때문에, **상태**라는 것을 고안

→ 상태를 이용하면 과거에 얽매이지 않고 **현재를 기반으로 객체의 행동 방식 이해 가능**

❗️하지만 'A'의 상태를 나타내는 기준은 객체가 아님을 명심
    ex) '공병주'라는 객체의 상태는 184cm, 74kg이지만, 184와 74의 **단순 값들은 객체가 아님**

### 💡 때로는 객체가 다른 객체의 상태를 나타내기 위한 경우 존재

  ex) 184cm, 74kg인 '공병주'라는 객체가 355ml양의 '콜라'라는 객체를 지님

→ 공병주의 상태는 키(값), 몸무게(값), 콜라(객체)로 표현 가능

✔️ **객체와 객체 사이의 의미있는 연결을 링크(Link)라고 칭함**

✔️ 객체를 구성하는 단순한 값은 **속성(Attribute)**라고 칭함

### → 모든 객체의 상태는 단순한 값과 객체의 조합으로 표현 가능 이런 객체의 상태를 구성하는 모든 특징을 통틀어 Property라고함

## ✔️ 객체의 상태는 객체에 정적인 Property와 동적인 Property 값으로 구성

### ❗️객체는 자율적인 존재라, 객체지향의 세계에서는 객체는 다른 객체의 상태에 직접적으로 접근할 수도, 상태를 변경할 수도 없음

→ 외부의 객체가 간접적으로 객체의 상태를 변경하거나 조회할 수 있는 **행동**이라는 것이 등장

---

# 행동

### 객체의 상태는 저절로 변경되지 않고 **객체의 자발적인 행동에 의해서만 바뀜**

→ 객체가 취하는 행동은 객체 자신의 상태를 변경시킴 ( Side Effect : 부수효과 )

✔️ 객체의 행동은 상태에 영향을 받음 ( 객체의 상태에 기반해 행동이 이루어진다는 뜻 )

→ 상호작용이 현재의 상태에 어떤 방식으로 의존하는가
ex) 거실에 있는 '공병주' 객체의 키가 184cm이기 때문에, 방으로 가는 180cm '문' 객체를 통과하지 못한다.

✔️ 객체의 행동은 상태를 변경시킴

→ 상호작용이 현재의 상태를 어떻게 변경시키는가
ex) 74kg '공병주' 객체가 300kcal의 '햄버거' 객체를 300개 먹었더니 76kg가 되었다.

### → 과거의 행동들을 확인 할 필요 없이 행동을 하는 시점의 Property만 이용하면 행동 가능

---

# 협력과 행동 ( 협력하는 객체들의 공동체 )

### ✔️ 어떤 객체도 섬이 아님 → 객체는 자신에게 주어진 책임을 다하기 위해 다른 객체와 협동

### ✔️ 객체가 다른 객체와 협력하는 유일한 방법은 다른 객체에게 요청을 보내는 것

### ✔️ 객체는 다른 객체와 메세지를 통해서만 의사소통 가능

→ 객체는 수신한 메세지에 따라 적절히 행동하고 협력에 참여하고 그 결과로 자신의 상태를 변경

### 💡 객체는 행동을 통해 다른 객체와 협력해야하므로 행동은 외부에 가시적이어야 함

---

# 상태 캡슐화

### 현실 세계의 객체와 객체지향 세계의 중요한 차이

→ 현실 세계 속에서 '공병주'라는 객체는 '콜라' 객체를 마시는 능동적인 존재이지만
'콜라'라는 객체는 현실 세계에서 아무것도 할 수 없는 수동적인 존재

→ 하지만, 객체지향 세계 속에서 **모든 객체는 '자신의 상태를 스스로 관리하는 자율적인' 존재**

'공병주' 객체는 '콜라' 객체를 먹고 직접 자신의 몸무게 상태를 바꾸는 것처럼
'콜라' 객체도 '공병주'에게 먹힌 후, 남은 콜라 양 상태를 바꾸는 주체는 '콜라' 객체여야함.

### ✔️ 따라서, '공병주' 객체는 '콜라' 객체의 '남은 양'이라는 상태를 직접 변경할 수 없고
'콜라' 객체에게 콜라를 마셨다는 메시지를 전달할 수 밖에 없음

→ 따라서, '공병주'는 '콜라'를 마시고 자신의 '몸무게 상태'를 증가하고 내가 마신만큼 '콜라'의 '남은 양 상태'를 줄여돌라는 요청만을 할뿐. 또한, **'콜라'의 '남은 양 상태'를 줄일지 말지는 메세지를 수신한 '콜라'가 결정할 사항**
**'공병주'는 '콜라'의 '남은 양 상태'가 줄었는지 안줄었는지 알 수 없음.**

## 캡슐화

### → 추상적인 캡슐이라는 것 안에 상태를 외부로 노출시키지 않고, 행동만을 외부에 노출시킴. 또한, 외부에서 객체에 접근할 수 있는 것은 오직 행동

ex) 에어컨에 온도up, 온도down, 온도check 3가지 버튼이 있다고 생각해보자. 세 가지 버튼은 외부에 노출된 행동이다. 또한 온도 up과 온도 down 행동은 온도라는 '상태'를 변경할 수 있다. 온도 check를 누르면 '온도 상태'를 알 수 있다.

💡' 여기서 온도는 외부에 노출시키지 않는다며? '라는 질문에 대한 자문자답

→ 생각해보면 '나'라는 객체가 에어컨의 온도 check라는 버튼을 눌러 '에어컨' 객체에게 **"너의 온도를 보여줘"라는 메세지를 던질 뿐, 그 응답에 응할지 말지는 에어컨 객체가 자율적으로 선택하는 것**이라고 생각한다.

→ 또한, 온도 up과 온도 down을 하는 시점에선 온도 check 버튼을 누르지 않았기 때문에, 온도라는 상태에 대해서는 **외부로 노출시키지 않는 것**이라고 생각한다

### ✔️ 객체의 자율성 ⬆️ : 외부 객체가 자신의 상태 변경을 기대하더라도, **자신에게 메세지를 보내는 것 말고 어떠한 간섭도 불가**

→ 협력에 참여하는 객체들의 협력이 유연하고 간결해짐.

---

# 식별자 : 값과 객체

### 객체가 식별가능 하다는 것은 객체가 Property를 가지고 있다는 것

→ Property에 기반하여 서로 다른 여러 객체들을 구분

## 값

### 값은 숫자, 문자열, 시각, 금액 등의 변하지 않는 양을 모델링
→ 값의 상태는 불변

💡 ' 시간의 흐름에 따라 시각은 바뀌는데 왜 불변이지? ' 라는 것에 대한 자문자답

→ 10시에서 11시로 값이 바뀌는 것이아닌 10시가 하나의 값이고 11시가 하나의 값인 것이다. 
( 이 글을 읽는 누군가가 위의 저의 이해를 보고 틀린 이해라고 생각되시면 알려주시기 바랍니다
   bjuuuu98@gmail.com )

### 두 인스턴스의 상태가 같다면 두 인스턴스를 같은 것으로 판단

ex ) 종이에 'A'라는 글자가 두개 적혀있다면 사람들은 이를 보고 같은 글자라고 인식한다.

→ **상태에 따라** 두 값이 같은지 판단할 수 있는 성질 : **동등성(equality)**

### 값을 가르키는 용어 : 값 객체 ( value object )

## 객체

### 객체는 시간에 따라 변경되는 상태를 포함하며 행동을 통해 상태를 변경

→ 객체는 가변 상태를 가짐. 따라서, 상태를 기반으로 객체 동일함을 판단 가능

### 💡 객체의 상태가 같더라도, 두 객체는 독립적인 별개의 객체로 다뤄야한다.

ex) 이름과 키가 같은 두 개의 '객체'가 있더라도 이 둘은 다른 인격체

### ✔️ 따라서, 객체는 상태와 무관하게 다른 객체와 자신을 구분하는 식별자라는 Property를 가진다.

→ **식별자를 기반**으로 객체가 같은지를 판단할 수 있는 성질 : **동일성(identical)**

### 객체는 상태에 기반한 동일성 판단 불가 → 식별자를 통해 동일성 판단

→ 시간의 흐름에 따라 객체의 상태가 변하기 때문

### 객체를 가르키는 용어 : 참조객체( reference object ) or 엔티티( entity )

---

# 행동이 상태를 결정한다 : 상태를 중심으로 객체를 보지마라

## 상태를 먼저 결정하고 행동을 나중에 결정하는 방법의 악영향

### 1 . 캡슐화 저해

→ 상태에 초점을 맞출 경우, 상태가 외부 인터페이스에 노출 될 수 있어 캡슐화가 잘 되지 않는다.

### 2 . 객체를 협력자가 아닌 고립된 섬으로 만듦

→ 객체는 App에서 **다른 객체들과 협력**하여 객체들의 공통 목표인 프로그램의 원활한 수행을 위해 존재한다.
그런데 협력의 방식인 행동이 아닌, 상태를 중심으로 객체를 바라본다면 협력하지 못하는 객체를 창조할 것이다.

### 3 . 객체의 재사용성 저하

→ 같은 맥락에서의 뜻으로, 객체의 재사용성은 다양한 협력에 셀수 없이 많이 참여하는 능력에서 나온다.
그런데 협력에 참여하기 어려운 객체를 만든다면, 객체의 재사용성 역시 저하될 것이다.

## 객체를 결정하는 것은 객체의 행동

### ✔️ 새로운 객체를 만들 때, 특정 프로그램에서 협력하는 새로운 것이 필요하기 때문에 새로운 객체를 만드는 것이다. 따라서 넓게는 프로그램 전체 협력의 관점, 좁게는 협력을 하는 객체의 행동의 관점에서 객체를 설계해야한다고 생각한다

### ✔️객체가 전체에서 어떤 협력적인 행동을 해야하는지, 어떤 책임을 부여할지 결정을 하면, 자연스럽게 객체에 필요한 상태가 따라올 수 밖에 없다

### 책임-주도 설계

→ **객체의 행동은** 결국 전체에서 **객체의 책임**을 의미. 따라서, **어떤 책임이 필요한가**를 결정하는 과정이 전체 설계를 주도해야한다

---

# 은유와 객체

## '객체지향이란 현실 세계의 모방'이라는 말에 대한 문제

많은 사람들은 객체지향이란 현실 세계의 다양한 객체들을 모방 혹은 추상화하는 것이라고 생각한다. 
→ 현실 세계의 객체들을 관찰하고 그들의 특성을 간추리고 요약하여 소프트웨어 객체로 만들 수 있는, 추상화할 수 있는 능력이 중요하다는 생각이 기반한다.

### 하지만 객체지향은 현실 세계의 '단순 모방'이 아니다.

✔️소프트웨어의 객체들은 현실 객체와 전혀 다른 양상을 띈다.
ex) 소프트웨어 상품은 실세계의 상품이 못하는 가격책정과 같은 것들을 할 수 있다.

→ **소프트웨어 객체는 실세계의 객체를 단순 모방한 것이 아닌 특성이 다른 어떤 것이다.**

## 의인화

### 현실 객체와 소프트웨어의 가장 큰 차이점

✔️ 현실에서의 **수동적인 객체가 소프트웨어 객체로 구현될 때**, **해당 객체는 능동적인 객체로 변한다**.
ex) '공병주' 객체가 '마스크'객체를 휴지통에 버린다고 생각해보자. 마스크의 '위치 상태'는 공병주에서 휴지통으로 바뀌어야하는데, 객체지향에서 상태를 변경하는 주체는 **자기 자신뿐이다.** 그런데 실세계에선 **마스크가 자신의 위치를 바꿀 수는 없다.**

### ✔️이처럼 소프트웨어 객체가, 대응되는 현실의 객체보다 많은 일을 할 수 있는 소프트웨어 객체의 특징을 '의인화'라고 한다.

## 객체지향 세계는 현실 세계를 은유한 것이다

### 은유

→ 실제로는 적용되지 않는 한 가지 개념을 이용해 다른 개념을 서술하는 대화의 형태
→ 한 종류의 사물을 다른 종류의 사물 관점에서 이해하고 경험하는 것

✔️이 은유라는 개념을 통해, **소프트웨어 객체를 현실 객체에 빗대어(은유하여) 표현하고 설계하는 것**이다.

ex) 위에서 들었던 마스크를 예시로 들면, 실세계 상의 마스크는 소프트웨어 상의 마스크처럼 스스로의 위치를 바꿀 수는 없어 같은 것 혹은 모방한 것이라고 표현하기 보단, 소프트웨어 상의 마스크를 실세계 상의 마스크에 빗대어 구조화하고 설계한다고 표현하는 것이 맞다고 생각한다

### 표현적 차이

✔️실제 객체의 이름과 이를 빗댄 소프트웨어 객체의 이름을 같게 혹은 비슷하게 하여 표현적 차이를 줄이자.
→ 소프트웨어의 **구조를 쉽게 예**측할 수 있으며, 해당 객체의 **책임을 어느정도 쉽게 이해하고 파악**할 수 있다.

### 💡 결론적으로, 객체지향에서의 목적은 현실을 모방하는 것이 아닌, 현실 세계를 빗대어 소프트웨어 세계를 설계하고 소프트웨어 객체의 이름 역시 현실 세계에 대응하는 객체의 이름에 빗대어 혹은 동일하게 사용하여 객체의 특성을 잘 이해할 수 있도록 하는 것이다.