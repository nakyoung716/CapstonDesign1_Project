# CapstonDesign1_Project
Smart Saver

# Partner
> philip : back-end<br>
> nakyoung : front-end<br>
> sukwoo : back-end<br>
> seungchule : front-end

# Title
> 초음파 센서를 통한 전력 차단기

# 무엇을 만드는가, 왜 만드는가
> 집에 설치된 인체 감지 센서(초음파 센서)를 통하여 집을 일정시간 비우면 자동으로 가구의 전력을 차단해주는 것,
사용하지 않는 플러그의 대기전력을 자동으로 차단함으로써 전기요금을 절약할 수 있음

# 3. 시스템 구성도  
> ![Alt text](/diagram.jpg)  <img width="515" alt="img" src="https://user-images.githubusercontent.com/46955861/56109982-bbf60200-5f8d-11e9-92a2-7874157ada79.png" width="700" height="350"><br>  

# 데이터 흐름도
> 1) 초음파 센서를 이용해 집 안에 사람이 있는지 판단 (아두이노)  
> 2) 초음파 센서로 인체 감지 후 인체 감지 데이터를 DB에 저장  
> 3) DB로 부터 받아온 정보로 확인했을 때 일정 시간(t) 이상 움직임이 없다면 전력을 차단(아두이노)  
> 4) 차단된 전력량을 DB에 저장  
> 5) 웹 사이트에 절약한 전력량 등 정보를 출력  
> 6) 사용한 전력량을 통해 이번 달 전기요금 예상, 집을 비운 시간의 누적 데이터를 통해 지정한 시간(t)을 조절 등 추가적인 가치를 얻음  

# 예시  
> 초기 일정시간 설정 = t(ex : 10분)  
t분 이상 집을 비우면 움직임, 인체 센서를 통해 전력 차단  
1주일 단위로 집 비운 시간 데이터를 축적  
데이터를 기준으로 t를 자동으로 조절  
(ex : 집을 평균적으로 1시간 이상 비우면 t를 1분씩 줄임)  
(ex : t가 10분일때 평균적으로 집을 비운 시간이 20분 정도로 큰 차이가 없는 경우 전력을 껐다, 켰다 하는 것이 더 소모가 되므로 t를 증가)

# 멘토의견
> 김수보 : 
집에 있을 때, 없을 때를 어떻게 판단할 것인가
데이터를 어떻게 활용할건지 계획수립도 되면 좋겠음.
복잡하지 않고, 간단한 수준의 접근도 괜찮음. 
