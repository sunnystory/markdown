# 1102 PM progression project (personal)

1. **표준화** **!!** 

   > 표준화 값의 빈도분포 그림 필요 **!!**

2. **장바구니 연관분석   **       ->**???**
3. deer 데이터 회귀?
4. 앱크롤링?



5. 대중교통 접근성 !!??? 박성준님 질문



#### progress ppt 준비

대본

> 아직까지 시사할만한 결과가 나오지 않아, 데이터 처리 위주로 내용 넣음

연관성 분석 mc 질문

> 장바구니 분석이 처음보는 알고리즘인데 잘 이용할 수 있을 것 같아서 사용하려고 하는데요.
>
> 혹시제가 개념을 잘못 이해했나 싶어서요!
>
> 1. 제가 하는 분석에서 기준이 6개가 있을때 각 기준마다 동일하게 나올 수 있는 item들이 있다면,
>
> 각 기준별 나타나는 item의 빈도로 연관성 분석을 진행할 수 있을까요?
>
> 6개의 기준이 있다고 했을때, 6개 기준의 교차 분석을 하는데 
>
> 기준마다 공통적으로 몇번이상 나오는 item들을 선정해서 제일 지지도가 높은 item을 선정 하는 방법으로 이렇게  item끼리의 연관성이라기보다는 기준내에서 겹치게 되는 item들의 연관성을 분석하는데 이용할 수 있을지 싶어서요!
>
> 2. 그리고 연관성 분석 개념에 신뢰도가 있는데 
>
>    예제에서 지지도만 확인하고 신뢰도 구하는 방법은 못봤던 것 같아서요!
>
>    혹시 apriori algorithm이 신뢰도도 구할 수 있는 알고리즘이라면, 기준 A에 나타나면서 기준 A와B에 공통적으로 나타내는 item을 선정해 신뢰도를 구하는 방법도 생각할 수 있는 걸까요?  
>
> 3. 
>
>  이 장바구니 알고리즘을 이용할 수 있을지

> 1번의 답변...
> 보내준 내용만으로는 딱 감이 오지는 않는데요..
> 그래도 시도해볼만 한거 같아요...
>
> 2번의 답변...
>
> [ 연관 분석에서의 지지도와 신뢰도 ]
> A와 B상품의 지지도 = A상품과 B상품을 같이 구입한 횟수 / 전체 구매 횟수
> A상품에 대한 B상품의 신뢰도 = A상품과 B상품의 동시출현 횟수 / A상품의 출현 횟수
>
> 지지도는 "동시 출현 개수 / 전체 구매리스트"
> 신뢰도는 "동시 출현 개수 / 기준 상품 리스트" 
>
> 위의 식대로라면 지지도는 절대 신뢰도보다 높을 수 없으며 같거나 낮을 수 밖에 없는 수치이다.
>
>
> 지지도만으로도 일정 이상의 데이터만으로 연관성을 파악할 수 있으며, 특정 이상값의 신뢰도를 
> 추천한다는 경우에는 신뢰도까지 파악하여 처리하게 된다.
>
> 그리고 신뢰도는 association_rules()라는 함수로 구할 수 있어요...
> 점검해볼만한 소스를 준비해서 드릴께요.

#### 연관성 분석으로  가중치 함수 구하는 flow보다의 장점 찾아보기

> 할 수 있을지 모르겠지만, 그걸 강조하기 위해서는 다른방법 대신 이 방법을 쓰는 이유가 무엇인지를 좀더 justify할 필요가 있을 것 같음
>
> 교차분석 말고 다 지표화해서 가중치를 계산한다음 하나의 지표로 만드는게 적용하기는 훨씬 쉬운데.
>
> 가중치가 선정하기 어렵다고 생각하기에 그부분을 어떻게 풀것인가가 또 한편으로 연구의 contribution이 될 수 있을것 같다는 생각이 듬 