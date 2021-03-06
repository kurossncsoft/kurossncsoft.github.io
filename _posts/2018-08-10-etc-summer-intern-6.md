---
layout: post
title: "인턴 생활기 #6"
date: 2018-08-10 18:00:00
categories: ETC
author : DANBI
cover: "/assets/title6.png" 
---



인턴 생활도 어느덧 마지막을 향해 달려가고 있습니다. 다음 주가 말복이기도 하고 연일 최고 기록을 갱신하는 무더운 날씨에 함께 힘을 북돋우고자 오늘 점심 회식을 다녀왔는데요. 햇살은 따가웠지만 회사 안에만 있다가 외출도 하고 장어덮밥도 먹으니 정말 좋았습니다!ㅎㅎ 


<p align="center">
<img src="/assets/etc/summer_intern/unagi_gang.jpg" style="width:6in" />

</p>

### 변화무쌍한 유저들의 전투행태

지난 포스팅에서는 리니지M의 중요한 플레이 요소인 PvP 시스템과 유저별 전투 유형에 대한 소개를 했었습니다. 일별로 일정한 기준에 따라 혈맹전투자, PvP공격자, PvP피해자, 동일혈맹전투자, 단발성전투자 등으로 유형을 구분하고 그에 따른 소비 패턴에 대한 간단한 분석 결과를 공유했었습니다. 이번 포스팅에서는 소비 이외의 플레이패턴에 대한 분석 내용을 소개하려 합니다! 리니지M에서 유저들의 전투유형은 일별로 할당되므로 특정 기간의 전투유형을 살펴보게 될 경우 전투 유형이 매일 바뀌는 유저도 있을 것이고 늘 같은 유형으로만 분류되는 유저도 존재합니다. 따라서 이렇게 변화무쌍한 유저들을 비슷한 전투 성향을 지닌 유저들끼리 그룹화 할 때에는 빈번한 유형뿐만 아니라 그 유형이 변화되어온 순서까지도 고려해 주어야 하는데요. 이해를 돕기 위하여 아래와 같은 표를 그려보았습니다.



<p align="center">
<img src="/assets/etc/summer_intern/table.PNG" style="width:8in" />

</p>



위의 표는 일별로 각 유저들의 전투 유형을 나타냅니다. 유저 A처럼 처음에는 전투를 즐기지 않다가 혈맹에 가입한 후 혈맹전을 많이 할 수도 있고, 유저 B처럼 혈맹전을 하다가 혈맹에서 탈퇴하고 PvP전투를 제외한 다른 활동만 할 수도 있습니다. 이때 이 두 유저는 혈맹 전투자였던 기간과 전투가 없었던 기간이 동일하지만 그에 대한 순서가 다릅니다. 이러한 순서까지도 고려하여 비슷한 유저들끼리 그룹화 하고자 하는데, 이를 위한 분석 중 하나가 바로 Sequence Clustering입니다. 저희는 지난 2017년 11월 29일에 오픈했던 리니지M의 신서버 ‘블루디카’ 중 하나의 서버를 선택했고 오픈 직후로부터 4주간의 데이터를 추출하여 분석했습니다.

### 신서버 오픈, 그리고 PvP 전투의 증가

먼저, 일정 기간 이상 접속했던 유저를 중심으로 살펴보기 위해 7일 연속 미접속한 유저들은 분석 대상에서 제외하고 Sequence Clustering을 하여 아래와 같은 5가지 유형으로 나누어 보았습니다. 



<p align="center">
<img src="/assets/etc/summer_intern/seq_clust.PNG" style="width:8in" />

</p>



그렇다면 이렇게 나누어진 5개의 유형별로 플레이에는 어떤 차이가 있을까요? 아래의 그림은 Sequence Clustering을 통해 나누어진 각각의 그룹별로 캐릭터들이 4주간 죽은 총 횟수입니다. 흥미로운 점은 전반적으로 PvP피해자 그룹의 죽은 횟수 보다 혈맹 전투 그룹이나 호전적인 PvP성향을 띠는 유저들의 죽은 횟수가 더 많다는 것인데요. 대체적으로 PvP피해자 집단은 다른 캐릭터에게 공격을 당하면 바로 도망가버리는 경우가 많고, 전투가 많은 유저들은 그에 맞서 싸우는 경우가 많아 이러한 결과를 보이는 것 같습니다.  



<p align="center">
<img src="/assets/etc/summer_intern/die_box.png" style="width:8in" />  

</p>



이처럼 일별로 집계된 전투 유형을 하나의 수열로 보고 그룹화한 후 유저들의 플레이패턴을 분석한다면, 수많은 유저들을 하나하나 분석하는 것보다 흥미로운 결과를 도출할 수 있습니다. 또한 유형별로 특징들을 눈에 띄게 알 수 있고, 역으로 X 특징들을 갖는 유저들은 Y 전투 유형이라고 알아낼 수도 있겠죠. 그렇다면 여기서 한 가지의 의문점이 생길 수 있습니다. 과연 전투 유형으로 나누어진 유저들의 전투 외적인 게임 플레이 패턴도 서로 다르게 나타날까요? 

### 전투 이외의 다양한 게임 내 활동

이를 알아보기 위하여 대상 유저들의 전투와 관련된 활동 지표를 제외한 다른 플레이 기록만을 토대로 주성분 분석을 해보았고 다음과 같은 결과를 얻을 수 있었습니다.

<p align="center">
<img src="/assets/etc/summer_intern/pca_var.JPG" style="width:8in" />  

</p>

리니지M에서 할 수 있는 다양한 활동들이 유사한 성격을 지닌 것끼리 묶인 것을 보실 수 있는데요. 첫번째로 살펴볼만한 것은 소셜 활동입니다. 게임 내에서 친구 신청/수락/삭제를 했던 횟수와 혈맹 가입/탈퇴 횟수, 채팅 횟수 등이 1사분면 방향으로 함께 뻗어있는 것을 보실 수 있습니다. 다음으로 주목할만한 것은 게임 내 캐쉬인 다이아 소비, UI상점의 상품 구매 개수, 거래소 구매 횟수 등 소비와 관련한 플레이 기록이 4사분면 내에서 화살표가 비슷한 방향을 가리키고 있다는 것입니다. 마지막으로는 거래소 판매 횟수, 아이템 제작 횟수 등 생산적인 활동이 한 데 묶인 것을 볼 수 있겠네요. 이렇게 비슷한 성질의 활동들끼리 묶인 상태에서 각 유저들에게 앞서 분류했던 5개의 전투 유형 레이블을 달아보겠습니다. 

<p align="center">
<img src="/assets/etc/summer_intern/pca_biplot.JPG" style="width:8in" />  

</p>

한눈에 보기에도 유형 A가 전반적으로 많은 활동량을 보인다는 것을 알 수 있는데요. 유형 A는 앞선 Sequence Clustering에서 나누어진 혈맹 전투가 많은 유저들의 집단입니다. 또한 유형 B에 해당하는 호전적인 PvP성향을 가진 유저들 중에서는 소셜 활동이 활발한 유저가 많은 것으로 보여지는데요. 전투뿐만이 아니라 전반적으로 다양한 활동들을 즐기는 유저가 많다고 볼 수 있겠습니다. 반면 전투에 다소 소극적인 성향을 가진 집단인 C, D, E의 경우에는 전반적인 활동량이 적은데요. 특히 소셜 관련 활동이 소비나 생산과 관련한 활동보다 두드러지게 적은 것으로 보입니다. 이렇게 유저들을 전투 유형으로 나누었음에도 불구하고 전투 이외의 플레이 패턴에도 차이가 있다는 것은 아주 흥미로운 사실이 아닐 수 없습니다. 그렇다면 이 전투 유형이나 플레이 성향이 레벨업 속도에도 과연 영향을 미칠까요?

### 캐릭터 성장 속도에 미치는 영향 

저희는 분석에 앞서 여러 가지 추측을 할 수 있었는데요. 전투나 소셜 활동이 많은 캐릭터는 상대적으로 사냥을 덜 해서 레벨업이 더딜 것이라는 추측도 있었고, 반대로 전투를 좋아하는 유저는 더 많은 유저들을 공격하기 위해 높은 레벨에 빠르게 도달할 것이라는 추측도 있었습니다. 

이런 추측들을 확인해 보기 위하여 여러 요인에 따른 레벨업 속도를 LASSO Regression를 통해 분석해 보았는데요. 앞서 군집화했던 유형에 속하는 유저들 중 레벨 55이상 달성한 유저들의 1업당 소요 시간을 모델링 해보았습니다. 전투 유형, 플레이 시간, 전투 횟수, 일반 채팅 횟수, 다이아 소비량, 친구 수락/삭제/요청 횟수, 혈맹 가입/탈퇴 횟수 등 수많은 게임 요소들 중에서 레벨업 소요 시간에 영향을 주는 것은 무엇일까요? 그리고 어떤 플레이들이 빠른 레벨업에 도움이 될까요? LASSO Regression을 통해 추정된 회귀계수와 결과를 분석해보면 다음과 같이 정리할 수 있습니다. 

<p align="center">
<img src="/assets/etc/summer_intern/reg_result.PNG" style="width:8in" />  

</p>

모형의 종속 변수를 1업당 소요 시간으로 설정하였으므로, 추정된 회귀계수가 양수인 경우에는 레벨업 속도를 더 느리게 하는 요인이고, 음수인 경우에는 빠른 레벨업에 도움을 주는 요인으로 해석할 수 있습니다. 따라서, 레벨업에 도움이 되는 요인은 UI 상품 구매량, 죽은 횟수, 아이템 제작 횟수, 시련던전 도전 및 성공 횟수로 해석할 수 있고, 방해가 되는 요인은 유저간 전투 횟수와 거래소 구매 횟수로 해석할 수 있습니다. 흥미로웠던 점은 전투 유형에 따라서도 레벨업 속도가 다르다는 것이었습니다. 

위의 결과에 의하면 호전적인 PvP성향을 띠는 유형 B 유저들는 상대적으로 레벨업 속도가 빠르고, PvP공격을 많이 받는 유형 C 유저들은 레벨업 속도가 느릴 것입니다. 이는 PvP공격을 당함으로써 사냥에 다소 방해를 받아 레벨업이 더딘 것으로 추측할 수 있습니다. 또한 레벨이 오를수록 레벨업에 필요한 절대적인 경험치량이 더 많으므로, 현재 레벨이 높으면 레벨업이 더 느리다는 결과는 합리적인 것으로 보입니다.

지금까지 리니지M 유저들의 전투 유형 및 플레이 패턴을 분석한 내용을 소개해 봤는데요. 사실 게임 데이터를 처음 분석해 보았기 때문에 여러 가지 시행착오를 겪기도 했습니다. 하지만 멘토님들께서 꼼꼼하게 잘 알려주신 덕분에 무사히 과제를 끝낼 수 있었습니다! (이 자리를 빌어 I&I실의 모든 분들께 감사의 인사를 드립니다♥) 

분석 과제를 수행하면서 느낀 점도 참 많았는데요. 특히 게임 로그의 다양성이 상상을 초월했습니다. 게임별로 약 200가지의 액션 마다 60여 가지의 정보가 기록되기 때문에 로그 자체에 대한 이해에도 시간이 걸렸는데요. 수많은 DB 테이블을 비롯한 로그 정보들을 모두 머릿속에 가지고 계신 멘토님들이 정말 대단해 보였습니다.ㅎㅎ 여러 데이터를 접하면서 하루에 274번 죽은 캐릭터와 같이 특이한 유저들도 발견하게 되었는데, 이러한 유저들을 포함하여 분석을 하는 것이 어렵기는 했지만 한편으로는 흥미로웠습니다. 그리고 무엇보다도 자신이 분석하는 게임에 대한 전반적인 이해가 필수적이라는 것을 깨닫게 되었습니다. 왜 인턴 사전 과제가 리니지M 55레벨 달성이었는지 데이터를 보고, 분석을 하면서 몸소 느꼈습니다. 사실 지금도 꾸준히 플레이를 하고 있는데요. 자기 전에 자동 사냥을 켜놓고 아침에 일어나보면 어느새 죽어서 회복의 신녀 앞으로 이동해 있는 제 캐릭터를 보며 PvP피해자의 마음을 직접 이해하기도 했습니다.. ㅠㅠ 


<p align="center">
<img src="/assets/etc/summer_intern/lineageM.png" style="width:6in" /> 
지금도 열일 중인 내 캐릭...
</p>

6주라는 짧은 기간 동안 인턴 과제를 통해 처음 실무를 접해보면서 여러 가지 우여곡절도 많았지만 게임 데이터 분석에 관하여 많이 배웠던 뜻 깊은 시간이 되었습니다. 서툰 저희의 포스팅 끝까지 읽어주셔서 감사 드리고, 저희는 드디어 과제를 끝내고 사회에서의 첫 휴가를 만끽하고 오겠습니다.

그럼 저희는 휴가 다녀온 후 다음 주 마지막 인턴 생활기로 찾아 뵙겠습니다. 고맙습니다!

<p align="center">
<img src="/assets/etc/summer_intern/vacation.jpg" style="width:6in" />

</p>