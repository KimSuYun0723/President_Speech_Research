# President_Speech_Research
논문 "텍스트 마이닝을 활용한 대한민국 역대 대통령 연설문에 나타난 정치적 담론 분석" 연구에 사용했던 모든 소스 코드와 시각화 자료를 담은 레포지토리입니다. 
\\
아래는 폴더 및 파일의 역할에 대한 안내입니다.

# 1. 데이터셋(dataset)
## `dataset/raw_data`
크롤링을 통해 수집한 데이터 원본을 모아둔 폴더입니다.

## `dataset/cleaned_data`
크롤링을 통해 수집한 데이터에서, 전처리 과정을 거친 데이터를 모아둔 폴더입니다.

\\
# 2. 데이터 수집 및 전처리(crawling)
## `crawling/president_1_19`
1대 이승만 대통령부터 19대 문재인 대통령 연설문까지 크롤링 및 전처리하는 코드를 모아둔 폴더입니다. \\
Link : [대통령기록관](https://www.pa.go.kr/research/contents/speech/index.jsp)
- `./since_president_crawling.ipynb` : 크롤링 코드
- `./preprocessing_1_19.ipynb` : 전처리 코드

## `crawling/president_20`
20대 윤석열 대통령 연설문(~2024.07.02)까지 크롤링 및 전처리하는 코드를 모아둔 폴더입니다. \\
Link : [대한민국 대통령실](https://www.president.go.kr/president/speeches)
- `./president_office_crawling.ipynb` : 크롤링 코드
- `./preprocessing_20.ipynb` : 전처리 코드
- `./merge_csv.ipynb` : 나누어 실행하여 생성한 csv를 합치는 코드

\\
# 3. 빈도 분석 및 네트워크 분석(frequencyNnetwork)
## 3-1. 빈도 분석 결과 : `frequencyNnetwork/freq_result`
### `./top_30_keywords`
빈도수 상위 30개 단어들을 모아 시각화한 png 파일들을 모아둔 폴더입니다.

### `./total_counts`
각 대통령별로 사용했던 단어 당 빈도수를 계산하여 csv로 정리한 파일들을 모아둔 폴더입니다.

## 3-2. 네트워크 분석 결과 : `frequencyNnetwork/network_results`
대통령 별로 폴더가 정리되어 있습니다. 
각 폴더에는 다음과 같은 일정한 형식으로 정보가 저장되어있습니다.
- `./data` \\
: 네트워크 분석 시각화를 위한 노드(Node), 엣지(Edge), 행렬(Matrix)가 담겨있습니다.
- `./{대통령 이름} DR` \\
: Degree Report입니다. 총 3가지 통계량(Degree Distribution, Indegree Distribution, Outdegree Distribution)에 대한 시각화 결과물이 담겨있습니다. 이 모든 시각화 자료를 한눈에 볼 수 있는 html 파일도 함께 들어 있습니다.
- `./{대통령 이름} GDR` \\
: Graph Distance Report입니다. 총 4가지 통계량(Betweenness Centrality Distribution, Closeness Centrality Distribution, Eccentricity Distribution, Harmonic Closeness Centrality Distribution)에 대한 시각화 결과물이 담겨 있습니다. 이 모든 시각화 자료를 한눈에 볼 수 있는 html 파일도 함께 들어 있습니다. 
- `./{대통령 이름}_network.gephi`\\
: 네트워크 분석 시각화 툴인 Gephi 파일입니다. 
- `./{대통령 이름}.jpg` \\
: 최종 시각화 결과물입니다.

## 3-3. 빈도 & 네트워크 분석 코드
### `./num_of_speech_data.ipynb`
대통령별 연설문 데이터의 개수를 계산하는 코드입니다.

### `./total_network.ipynb`
대통령 연설문 전체를 대상으로 네트워크 분석을 수행하는 코드입니다.

### `./each_network.ipynb`
각 대통령을 대상으로 네트워크 분석을 수행하는 코드입니다.

# 4. 토픽 모델링-LDA 알고리즘(lda)
## `lda/result`
### `./result/each_result`
각 대통령을 대상으로 토픽 모델링 분석을 수행한 결과(html)를 모아둔 폴더입니다.
### `./result/group_result`
각 그룹(전체, 진보, 보수)을 대상으로 토픽 모델링 분석을 수행한 결과(html)를 모아둔 폴더입니다.
## `./LDA_group.ipynb`, `./LDA_kiwi.ipynb`
전자는 그룹(전체, 진보, 보수)을 대상으로, 후자는 각 대통령을 대상으로 토픽 모델링 분석을 수행한 코드입니다. 