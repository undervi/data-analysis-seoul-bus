# 서울시 생활 정보 기반 대중 교통 수요 분석

### 0️⃣ 기간 : 2023.08.21 ~ 2023.08.22<br/>

### 1️⃣ 미션 : 버스 노선 추가가 필요한 서울시 내 자치구 선정<br/><br/>

### 2️⃣ 데이터 : 생활이동 정보 등의 Tabular 데이터, csv 파일로 제공 (출처: 서울시 공공데이터 포털)
    1) 서울시 구별 버스 승하차 이용 데이터 / 서울시 버스 데이터
    2) 서울시 구별 생활 인구 데이터
    3) 서울시 구별 주민 등록 인구 데이터
    4) 서울시 구별 업종 등록 데이터
  
### 3️⃣ 목표 
    1) 새로운 도메인의 데이터를 파악한 후 적절히 처리하여 분석에 필요한 형태로 정리한다.
    2) 가설 수립, 단변량 분석, 이변량 분석, 가설 검증 등을 통해 비즈니스 인사이트를 도출한다.

### 4️⃣ 목차

1. [**구별 버스정류장 분석**](#bus)

2. [**구별 이동인구 분석**](#move)

3. [**구별 등록인구 분석**](#registration)

4. [**구별 업종 분석**](#industry)

5. [**최종 데이터 분석**](#final)

<br />

### 5️⃣ 느낀점
>데이터 분석을 배우고 처음으로 진행한 실전 팀 프로젝트라서 떨리기도 하고 걱정을 많이하면서 시작하게 되었다. 이번 프로젝트는 첫째날과 둘째날 오전에는 개인별로 데이터 처리와 분석을 하고 둘째날 오후에 조별 토의를 통해 최종적인 결과물을 내는 방식이었는데, 초반에는 혼자 이것저것 해보다가 추후에 조원들과 토의을 통해 더 좋은 결론을 낼 수 있어서 좋았다. 걱정과는 달리 재미있게 프로젝트를 잘 마무리 한 것 같아서 굉장히 뿌듯했다. 하지만 수치형 데이터들을 범주화하는 등 여러가지 방면에서 데이터를 가공해보지 못한 것이 아쉬웠어서 다음 프로젝트에서 꼭 적용해보려고 한다.

<br />



<div id="bus"> 
 
  ## 🚌 구별 버스정류장 분석 (1. 구별 버스정류장 분석.ipynb)

  >1 ) "서울시" 데이터만 추출, 결측치, 데이터프레임 합치기 등 가공 후 csv 파일로 저장한다. 
  <br/>2 ) 버스정류장 데이터를 활용하여 서울시 내 각 구별 정류장 수, 노선 수, 승하차 고객수를 분석한다.
  
  ```
  💡 분석 결과

    위 차트를 통해 알게된 사실을 정리해봅시다.
    1) 노선개수가 증가할수록 승차/하차평균승객수가 증가하는 경향이 있다.(중간정도 관계)
    2) 노선개수가 증가할수록 승차/하차총승객수가 증가하는 경향이 있다. (높은 관계)
    3) 정류장개수와 승차/하차평균승객수는 관계가 없다고 볼 수 있음 다만! 승차/하차총승객수와는 관련 있음 (높음)
  ```
  <br/>

  <div align="left">
    <img src="image/output.png" height="500" />
    <img src="image/output2.png" height="500" />  
  </div>

  <br/>
</div><br />

<div id="move"> 
 
  ## 🧑‍🤝‍🧑 구별 이동인구 분석 (2. 구별 이동인구 분석.ipynb)

  >서울시 생활이동 정보 데이터의 정보 확인 및 전처리 과정을 거쳐 필요한 데이터만 추출하여 저장한다.
  
  ```
  💡 분석 결과
    1) 유출이 제일 많은 구는? 강남구
    2) 유입이 제일 많은 구는? 강남구
    3) 유출이 제일 적은 구는? 금천구
    4) 유입이 제일 적은 구는? 금천구
  ```
  <br/>

  <br/>
</div><br />

<div id="registration"> 
 
  ## 🧑‍🤝‍🧑 구별 등록인구 분석 (3. 구별 업종 분석.ipynb)

  >서울시 내 각 구별로 등록된 인구 데이터의 정보 확인 및 전처리 과정을 거쳐 필요한 데이터만 추출하여 저장한다.
  <br/>자치구, 총 인구 수(계), 남자, 여자, 세대당 인구, 65세이상 고령자 컬럼을 추출했다.

  <br/>
</div><br />

<div id="industry"> 
 
  ## 🧑🏻‍🏭 구별 업종 분석 (4. 구별 업종 분석.ipynb)

  >서울시 내 각 구 별로 등록업종을 분석하고 필요한 데이터만 추출하여 저장한다.
  <br/>한식일반음식업 종사자수, 커피전문점 종사자수, 기타주점업 종사자수, 일반교과학원 종사자수, 한식육류요리전문점 종사자수 컬럼을 추출했다.
  
  <br/>
</div><br />

<div id="final"> 
 
  ## ✍🏻 최종 데이터 분석 (5. 데이터 분석.ipynb)

  >1 ) 지금까지 1~4에서 준비한 데이터 파일을 합친다. 
  <br/>2 ) 합쳐진 데이터프레임을 기반으로 데이터 분석을 진행한다.
  <br/>3 ) 최종적으로 버스정류장 개설이 필요한 자치구를 선정한다.
  
  ```
  💡 가설 수립

    1) 유효 면적과 정류장 수가 관련이 있을 것이다.​ - 유효면적: 자치구별 면적에서 실제로 생활할 수 있는 부분의 면적​

    2) 인구밀도별 택시 종사자 수와 정류장 수가 관련이 있을 것이다.​

    3) 인구밀도별 사업체 수와 정류장 수가 관련이 있을 것이다.​ - 택시 종사자, 운송업, 도매업 제외​

    4) 버스 수와 정류장 수가 관련이 있을 것이다.​ - 버스 수 = 승차총승객수/승차평균승객수​
    
    5) 65세이상고령자 수와 정류장 수가 관련이 있을 것이다.​

    => 분석 결과 송파구, 양천구, 강남구에 정류장 및 노선 증설이 필요하다.
  ```
  <br/>

  <div align="left">
    <p>가설 1</p>
    <p>유효면적(자치구별 면적에서 실제로 생활할 수 있는 면적)과 정류장 수는 비례한다는 결과를 얻을 수 있었다. 다른 가설에서 면적의 영향을 제외하고 계산하기 위해 feature에서 인구밀도가 아니라 유효면적별 인구밀도를 나누기로 한다. </p>
    <img src="image/output4.png" height="500" />
    <img src="image/output5.png" height="500" />  
  </div>
  <br/>

  <div align="left">
    <p>가설 2</p>
    <p>인구밀도 별 택시운송업 종사자 수가 많으면 택시의 수가 많기 때문에 버스 이용량이 적을 것이라고 생각해서 음의 상관관계일 것으로 예상했다. 하지만 이변량 분석을 실시해보니 약 0.35 정도의 양의 상관관계가 있었다. 이 흐름을 토대로 택시운송업 종사자 수/인구밀도 대비 정류장 수가 높을 수록 정류장수 포화도가 높다고 보았고, 정류장 포화도가 낮은 곳은 도봉구, 강서구, 노원구 등이 있었다.</p>
    <img src="image/output6.png" height="500" />
    <img src="image/output7.png" height="500" />  
  </div>
  <br/>

  <div align="left">
    <p>가설 3</p>
    <p>인구밀도 별 사업체 수가 많으면 상권이 형성되어 있다는 것이고, 대중교통의 수요가 있을 것이라고 예측했다. 예상대로 사업체수/유효면적인구밀도와 정류장 수는 약 0.4 정도의 양의 상관관계가 있었다. 이 흐름을 토대로 사업체수/유효면적인구밀도 대비 정류장 수가 높을 수록 정류장수 포화도가 높다고 보았다. 정류장 수 포화도가 낮은 곳은 종로구, 중구, 강남구, 서초구, 용산구이다. </p>
    <img src="image/output8.png" height="500" />
    <img src="image/output9.png" height="500" />  
    <img src="image/output10.png" height="500" />  
  </div>
  <br/>

  <div align="left">
    <p>가설 4</p>
    <p>승차총승객수/승차평균승객수(버스 수와 관련)과 정류장수*노선수는 약 0.75 정도의 양의 상관 관계가 있다. 추세에서 벗어날 수록 조정이 필요하다고 생각하면 그래프보다 상당히 아래 있는 구들의 정류장수 또는 노선수를 늘리면 좋을 것 같다. (중구, 동대문구, 양천구, 강남구, 송파구)​</p>
    <img src="image/output11.png" height="500" />
  </div>
  <br/>

  <div align="left">
    <p>가설 5</p>
    <p>65세 이상 고령자와 정류장수는 약 0.55 정도의 양의 상관관계가 있다. 이 흐름을 토대로 65세 이상고령자수/유효면적인구밀도 대비 정류장 수가 높을 수록 정류장수 포화도가 높다고 보았다. 정류장 수 포화도가 낮은 곳은 송파구, 양천구, 동대문구, 강동구, 광진구이다.</p>
    <img src="image/output12.png" height="500" />
    <img src="image/output13.png" height="500" />  
  </div>
  <br/>

  <div align="left">
    <p>최종</p>
    <p>여러가지 가설을 고려하여 계산했을 때 송파구, 양천구, 강남구가 정류장 포화도가 낮았다. 즉 해당 지역에 정류장 및 새로운 노선이 필요하다 </p>
    <img src="image/final2.png" height="500" />
    <img src="image/final1.png" height="500" />  
  </div>
  <br/>

  <br/>
</div><br />
