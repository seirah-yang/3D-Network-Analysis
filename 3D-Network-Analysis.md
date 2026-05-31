# 3D-Network-Analysis
3D Network Analysis: Pre/Post COVID 
[Scatter Plot: Pre/Post COVID](https://seirah-yang.github.io/3D-Network-Analysis/)

[Network-Analysis_3D version]()
## 입력 데이터
    1) rbqm_semantic_nodes.csv 
          → 노드 ID, 카테고리, 문헌 빈도(doc_frequency), 연결 강도(degree_strength), 매개 중심성(betweenness_centrality)
    2) rbqm_semantic_edges.csv 
          → 엣지 source/target, 가중치(weight), first_year, last_year
    3) rbqm_node_growth_summary.csv 
          → Pre/Post-COVID 비중, delta, is_new 분류

## 3D 네트워크 분석 모델 구성 
    1) 인터랙션 방법
    2) 드래그로 자유롭게 회전, 스크롤로 줌, 노드 클릭 시 하단에 상세 정보 패널 오픈
    3) 마우스를 노드 위에 올리면 Pre/Post-COVID 비중, 변화량, 문헌 수가 툴팁으로 표시

### 노드 인코딩
    1) 노드 크기는 전체 문헌 빈도에 비례하고, 색상은 갭 분석 상태를 표시 
    2) 초록(신규 등장), 주황(Post-COVID 성장), 붉은 계열(쇠퇴·갭 영역), 회색 계열(안정)
    3) 신규 등장 노드는 회전하는 링과 펄스 애니메이션으로 강조

### 엣지 인코딩
    1) 청록색 엣지는 2020년 이후 새롭게 형성된 Post-COVID 연결
    2) 회색 엣지는 Pre-COVID부터 존재하던 안정적 연결

### 필터 버튼 활용
    1) 상단 버튼으로 신규 등장, Post-COVID 성장, 쇠퇴, Pre-COVID 엣지를 각각 격리해서 구현
    2) 갭 분석의 각 레이어를 집중 탐색 가능
