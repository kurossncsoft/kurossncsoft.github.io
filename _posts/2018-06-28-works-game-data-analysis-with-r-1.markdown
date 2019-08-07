---
layout: post
title:  "R을 활용한 게임 데이터 분석 #1"
date:   2018-06-28 10:30:00
categories: Works
author : DANBI
cover:  "/assets/works/data_analysis_with_r/r_background_image.jpg"
---

**#데이터 분석가들이 가장 선호하는 언어**

R은 통계 분석을 하기 위해 개발한 언어이자 소프트웨어도구입니다. 원래 Bell 연구소에서 만든 ‘S’라는 프로그래밍 언어가 있었는데, 로버트 젠틀맨(Robert Gentleman)과 로스 이하카(Ross Ihaka)라는사람이 S를 참고해서 누구나 자유롭게 사용할 수 있도록 오픈 소스로 구현한 것이 R입니다(*눈치채셨겠지만 R이라는이름은 S라는 언어에서 비롯되었고 S라는 이름은 Statistics의 S를 뜻합니다).

R이 처음 공개된 게 1993년이니까, 벌써 20년이 넘은 오래된 언어네요. 그 동안 일부 통계학자들만 애용하는 마이너한 언어였는데, 최근 데이터분석 붐이 일면서 3~4년 사이 그 인기가 매우 높아졌죠.

아래 그림은 2015년,KDnugget(www.kdnuggets.com)라는 사이트에서 데이터 분석가들이 사용하는 도구를 조사한 자료입니다. 보시다시피 R은 데이터 마이닝 기반의 분석가들이 가장 많이 쓰는 도구임을 알 수 있죠. 이 사이트가 전통적인 통계 분석가들보다는 해커 성향(!)의 분석가들이 많이 이용하는 사이트라는 점을 감안하더라도, R이 상당히 대중화된 도구임을 알 수 있습니다.

<p align="center">
<img src="/assets/works/data_analysis_with_r/image_1.png" style="width:5in" />
캐글에서 조사한 데이터 과학자의 분석 도구 선호도 자료 <출처: [http://www.kdnuggets.com/2015/06/poll-programming-language-analytics-data-mining-data-science.html](http://www.kdnuggets.com/2015/06/poll-programming-language-analytics-data-mining-data-science.html)> 
</p>

여담이지만 엔씨소프트 데이터분석팀에서는 채용 시 지원자들에게 R을이용한 분석 과제를 냅니다. 과제를 낸 지 2~3년 정도됐는데, 초기엔 과제를 내는 지원자가 절반도 채 되지 않았지만 요새는 대부분이 과제를 너무 잘해 오셔서 깜짝 놀랄 때가 한 두 번이 아니랍니다(이참에 과제 난이도를 좀 올려야…^^;)

요즘은 통계학과에서도 R을 많이 사용한다더군요. 이런 것만 봐도 R은 이제 대세라도 봐도 무방할 것 같습니다.

<p align="center">
<img src="/assets/works/data_analysis_with_r/image_2.png" style="width:7in" />
캐글에서 조사한 데이터 과학자의 분석 도구 선호도 자료 <출처: [http://www.kdnuggets.com/2015/06/poll-programming-language-analytics-data-mining-data-science.html](http://www.kdnuggets.com/2015/06/poll-programming-language-analytics-data-mining-data-science.html)> 
취업 검색 사이트 Indeed.com에서 공개한 데이터 분석가 구직 추세 비교그래프 - 전통적인 통계 도구인 SAS, SPSS 가 추춤한 사이 R의 수요가 크게 높아졌다.
</p>

 **# R의 인기 요인**

그렇다면 왜 R은 이토록 인기가 많은 것일까요!? 제가 생각하는 몇 가지 이유를 꼽아 보겠습니다.

첫째, 데이터 시각화 기능이 다른 언어나 도구에 비해 매우 편리하고 풍부합니다. 통계 분석 도구에서 웬 시각화? 하고 생각하실 분들도 있을 텐데요, 실제 데이터 분석을 할 때는 많은 데이터를 적절한 그래프로 표현하는 게 매우 중요하답니다.

<p align="center">
<img src="/assets/works/data_analysis_with_r/image_3.png" style="width:5in" />
천 개의 숫자보다 더 나은 한 개의 그래프.jpg
</p>

둘째, 다양한 통계 분석 라이브러리가 있습니다. 일반적으로 널리 사용하는 회귀 분석이나 ANOVA(*분산분석), 기계 학습 알고리즘 등은 물론이고, 전세계의 수많은 통계학자와 개발자 및 분석가들이 자신들이 만든 분석용 알고리즘을 R로 구현해서 공개하고 있죠.

특히 최근에는 저명한 학자들이 논문을 통해 발표한 통계 분석이나 기계 학습 알고리즘을 R패키지로 함께 공개하는 경우가 많아 이런 최신 기법들도 R에서 편하게 사용해 볼 수 있습니다. 이건 다른 분석 솔루션에서는 얻을 수 없는 R만의 가장 큰 장점이죠.

가장 중요한 세 번째! 공짜입니다. 물론 공짜인 분석 도구들은 많이 있는데요, R은 성공한 오픈 소스의 장점인 빠른 발전을 통해 나날이 성능과 기능이 향상되고 있어 이젠 웬만한 상용 솔루션보다 나은 면이 많죠. 

여기서 잠깐. 물론 장점만 있는 건 아닙니다. R의 가장 큰 단점을 꼽자면, 프로그래밍 언어이기 때문에 프로그래밍 경험이 없는 사람에게는 상당한 진입 장벽이 있다는 거죠. 하지만 R은 다른 범용 언어와 달리 통계 분석에 특화된 언어이기때문에, 초심자가 데이터 분석 목적으로 배울 때는 다른 언어보다는 조금 쉬울 거라고 봅니다. (아니라고 하신다면…할 말은 없습니다만. 쿨럭.) 

엔씨소프트 데이터분석팀에서는 R을 대부분의 분석 작업에 사용할뿐만 아니라, 서비스 개발에도 적극 활용하고 있습니다. 최근에 R을 메인 도구로 사용한 대표적인 케이스는 ‘진성 유저 지표’ 작업인데요. 다음 편에서 이에 대한 이야기를 다뤄 보도록 하겠습니다.