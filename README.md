# President_Speech_Research
논문 "텍스트 마이닝을 활용한 대한민국 역대 대통령 연설문에 나타난 정치적 담론 분석"에 사용했던 자료 및 연구 결과물을 담은 레포지토리입니다.    
아래는 폴더 및 파일에 대한 안내입니다.

****
# 1. 빈도 분석 결과(freq_result)
## `./top_30_keywords`
빈도수 상위 30개 단어들을 모아 시각화한 png 파일들을 모아둔 폴더입니다.

## `./total_counts`
각 대통령별로 사용했던 단어 당 빈도수를 계산하여 csv로 정리한 파일들을 모아둔 폴더입니다.     

****
# 2. 네트워크 분석 결과(network_result/{번호}.{대통령이름})
대통령 별로 폴더가 정리되어 있습니다. 
각 폴더에는 다음과 같은 일정한 형식으로 정보가 저장되어있습니다.
## `./data`     
: 네트워크 분석 시각화를 위한 노드(Node), 엣지(Edge), 행렬(Matrix)가 담겨있는 폴더입니다.
## `./{대통령 이름} DR`     
Degree Report가 담긴 폴더입니다. 총 3가지 통계량(Degree Distribution, Indegree Distribution, Outdegree Distribution)에 대한 시각화 결과물이 담겨있습니다. 이 모든 시각화 자료를 한눈에 볼 수 있는 html 파일도 함께 들어 있습니다.
## `./{대통령 이름} GDR`     
Graph Distance Report가 담긴 폴더입니다. 총 4가지 통계량(Betweenness Centrality Distribution, Closeness Centrality Distribution, Eccentricity Distribution, Harmonic Closeness Centrality Distribution)에 대한 시각화 결과물이 담겨 있습니다. 이 모든 시각화 자료를 한눈에 볼 수 있는 html 파일도 함께 들어 있습니다. 
## `./{대통령 이름}_network.gephi`    
네트워크 분석 시각화 툴인 Gephi 파일입니다. 
## `./{대통령 이름}.jpg`     
최종 시각화 결과물입니다.     


****
# 3. 토픽 모델링-LDA 알고리즘(lda_result)
## `./each_result`
각 대통령을 대상으로 토픽 모델링 분석을 수행한 결과(html)를 모아둔 폴더입니다.
## `./group_result`
각 그룹(전체, 진보, 보수)을 대상으로 토픽 모델링 분석을 수행한 결과(html)를 모아둔 폴더입니다.
