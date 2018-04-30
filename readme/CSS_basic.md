### **CSS 의 구성**

----

<img width="405" alt="2018-04-30 2 43 05" src="https://user-images.githubusercontent.com/23162178/39416125-524b052e-4c85-11e8-89ad-93b0b7b3f78d.png">

* span : selector(선택자)
* color : property
* red : value



### **style 을 HTML 페이지에 적용하는 3가지 방법**

----

#### inline 

* HTML 태그 안에다가 적용한다.
* 다른 CSS 파일에 적용한 것 보다 **가장 먼저** 적용된다.

<img width="490" alt="2018-04-30 2 49 37" src="https://user-images.githubusercontent.com/23162178/39416164-be508794-4c85-11e8-938e-9c16753d882a.png">

#### internal

* style 태그로 지정한다.
* 구조와 스타일이 섞이게 되므로 유지보수가 어렵다.
* 별도의 CSS 파일을 관리하지 않아도 되며 서버에 CSS 파일을 부르기 위해 별도의 브라우저가 요청을 보낼 필요없다.

<img width="243" alt="2018-04-30 2 51 46" src="https://user-images.githubusercontent.com/23162178/39416190-08952b70-4c86-11e8-8bb4-4a55d839e538.png">

#### external

* 외부파일(.css)로 지정하는 방식
* css 코드가 아주 짧지 않다면 되도록 이 방식으로 구현하는 것이 좋음
* internal 코드와 같은 css 코드를 구현하고, style.css 같은 별도 파일로 만든다.
* 이후 아래처럼 link태그로 추가해준다.

<img width="320" alt="2018-04-30 2 54 55" src="https://user-images.githubusercontent.com/23162178/39416250-7868be08-4c86-11e8-99c2-60633a98ae9c.png">

#### 우선순위

Inline > internal > external



### **상속과 우선순위 결정**

---

* 상위에서 적용한 스타일은 하위에도 반영이 됨.


* **Box-model 이라고 불리는 속성들(width, height, margin, padding, border)** 와 같은 배치와 관련된 속성들은 하위 엘리먼트로 상속이 되지 않는다.

### **Cascading**

* CSS 는 여러가지 스타일 정보를 기반으로 최종적으로 **'경쟁**'에 의해 적절한 스타일이 반영된다.
* css 파일방식에 따른 차이

> *Inline > internal = external*
>
> Inline 방식으로 적용한 것이 가장 우선순위가 높고, internal과 external을 같은 우선순위를 갖는다.
>
> 예를 들어, 아래와 같이 코드상으로 internal 방식이 적용된 후, external 방식이 적용되는 경우 둘의 우선순위가 같기 때문에 css.css 파일에서 div의 색을 blue 로 설정한다면 나중에 적용된 external이 채택되어 최종적으로 blue 가 되는 것이 맞다.
>
> <img width="313" alt="2018-04-30 3 02 01" src="https://user-images.githubusercontent.com/23162178/39416380-76b5d978-4c87-11e8-9444-6e9981292896.png">



* element 에 따른 차이

> element 간 우선순위는 id > class > html 태그 속성 이다.
>
> <img width="245" alt="2018-04-30 3 08 59" src="https://user-images.githubusercontent.com/23162178/39416517-7b6d5850-4c88-11e8-98de-fad1952f100e.png">
>
> 위의 경우 가장 우선순위가 높은 id 의 설정값인 red 가 text의 색으로 설정된다.

* 선언 방식에 따른 차이

> 같은 선택자(selector)라면 **나중에 선언**된 것이 반영된다.
>
> 선택자의 표현이 **더 구체적인 것**이 더 우선순위가 높다.
>
> * body > span (o)
> * span (x)





### **CSS selector**

---

HTML 의 요소를 tag, id, html 태그 속성 등을 통해 쉽게 찾아주는 방법

#### **element 에 style 지정을 위한 3가지 기본 선택자**

* Tag 로 지정하기

<img width="221" alt="2018-04-30 3 20 34" src="https://user-images.githubusercontent.com/23162178/39416734-53ec0d10-4c8a-11e8-9f62-cca56817444d.png">

* id 로 지정하기

<img width="435" alt="2018-04-30 3 20 40" src="https://user-images.githubusercontent.com/23162178/39416745-73101042-4c8a-11e8-95ed-e03291e0d35f.png">

* class 로 지정하기

  <img width="407" alt="2018-04-30 3 20 46" src="https://user-images.githubusercontent.com/23162178/39416759-88aa4602-4c8a-11e8-809f-5ba43ece617d.png">

이들을 혼합해서 사용해 선택하는 방법도 있다.

