```js
---
config:
  layout: cose
---
```

|Layout|특징|
|---|---|
|`dagre`|**기본값**, 계층형 그래프에 적합|
|`elk`|**복잡한 그래프 자동 배치에 강함**|
|`tidy-tree`|트리 구조를 깔끔하게 정렬|
|`cose`|네트워크처럼 연결관계 중심으로 배치|
|`elk` 계열 옵션|방향·간격 등을 세밀하게 조정 가능|

## layout: dagre

```mermaid
---
config:
  layout: dagre
---
flowchart LR
    A["요구사항 분석"] --> B["설계"]
    A --> C["개발"]
    B --> D["테스트"]
    C --> D
    B --> E["문서화"]
    C --> F["배포"]
    D --> F
    E --> F
```

```mermaid
---
config:
  layout: dagre
---
flowchart LR
    A --> B
    A --> C
    B --> D
    C --> D
    B --> E
    C --> F
    D --> G
    E --> G
    F --> G
```

## layout: elk

```mermaid
---
config:
  layout: elk
---
flowchart LR
    A["요구사항 분석"] --> B["설계"]
    A --> C["개발"]
    B --> D["테스트"]
    C --> D
    B --> E["문서화"]
    C --> F["배포"]
    D --> F
    E --> F
```

```mermaid
---
config:
  layout: elk
---
flowchart LR
    A --> B
    A --> C
    B --> D
    C --> D
    B --> E
    C --> F
    D --> G
    E --> G
    F --> G
```

# chart 종류

## [[flowchart]]

```mermaid
flowchart LR
    A --> B --> C
```

## sequenceDiagram

```mermaid
sequenceDiagram
    Client->>Server: 요청
    Server-->>Client: 응답
```

## classDiagram

```mermaid
classDiagram
    User --> Order
    Order --> Product
```

## erDiagram

```mermaid
erDiagram
    USER ||--o{ ORDER : places
    ORDER ||--|{ PRODUCT : contains
```

## stateDiagram-v2

```mermaid
stateDiagram-v2
    [*] --> 대기
    대기 --> 실행
    실행 --> 완료
    완료 --> [*]
```

## journey

```mermaid
journey
    title 쇼핑 사용자 여정
    section 상품 탐색
      검색: 5: 사용자
      상품 확인: 4: 사용자
    section 구매
      장바구니: 4: 사용자
      결제: 3: 사용자
```

## gantt

```mermaid
gantt
    title 프로젝트 일정
    dateFormat YYYY-MM-DD

    section 개발
    설계 :a1, 2026-09-01, 5d
    개발 :a2, after a1, 10d
    테스트 :a3, after a2, 5d
```

## pie

```mermaid
pie title 운영체제 점유율
    "Linux" : 40
    "Windows" : 35
    "macOS" : 25
```

## gitGraph

```mermaid
gitGraph
    commit id: "초기"
    branch develop
    checkout develop
    commit id: "개발"
    checkout main
    commit id: "수정"
    merge develop
```

## timeline

```mermaid
timeline
    title 네트워크 발전
    1960s : ARPANET
    1980s : TCP/IP
    1990s : Internet
    2000s : Web 2.0
```

## quadrantChart

```mermaid
quadrantChart
    title "Technology Priority"
    x-axis "Low Difficulty" --> "High Difficulty"
    y-axis "Low Importance" --> "High Importance"
    quadrant-1 "High Importance / High Difficulty"
    quadrant-2 "High Importance / Low Difficulty"
    quadrant-3 "Low Importance / Low Difficulty"
    quadrant-4 "Low Importance / High Difficulty"
    "Feature A": [0.2, 0.8]
    "Feature B": [0.8, 0.9]
    "Feature C": [0.3, 0.3]
    "Feature D": [0.7, 0.2]


```

## requirementDiagram

```mermaid
requirementDiagram

    requirement system_req {
        id: "REQ-001"
        text: "dfsdf"
        risk: High
        verifymethod: Test
    }

    element PLC {
        type: "system"
    }

    PLC - satisfies -> system_req


```

## C4Context

```mermaid
C4Context
    title 시스템 구성

    Person(user, "사용자")
    System(system, "모니터링 시스템")
    System_Ext(db, "데이터베이스")

    Rel(user, system, "사용")
    Rel(system, db, "조회")
```

## sankey-beta

```mermaid
sankey-beta
MainJob,5000,Salary
SideHustle,1000,Salary
InvestReturns,500,Salary
Salary,2500,FixExpenses
Salary,1500,VariableExpenses
Salary,2000,Savings
Salary,500,Investment
FixExpenses,1200,Rent
FixExpenses,800,Insurance
FixExpenses,500,Loans
VariableExpenses,800,Food
VariableExpenses,400,Shopping
VariableExpenses,300,Leisure
Savings,1500,EmergencyFund
Savings,500,SubscriptionSavings
Investment,500,Stocks


```

## xychart-beta

```mermaid
  xychart-beta
    title "월별 데이터"
    x-axis ["1월", "2월", "3월", "4월"]
    y-axis "값" 0 --> 100
    bar [30, 50, 40, 70]
    line [30, 50, 40, 70]
```

## block-beta

```mermaid
block-beta
    columns 3

    A["사용자"]
    B["서버"]
    C["DB"]

    A --> B
    B --> C
```

## architecture-betaㅁ

```mermaid
architecture-beta
    group api(cloud)[API]

    service server(server)[Server] in api
    service db(database)[Database]

    server:R --> L:db
```

```mermaid
treeView
			root/
			├── src/
			│   ├── components/
			│   │   ├── Button.tsx
			│   │   └── Modal.tsx
			│   └── App.tsx
			├── package.json
			└── README.md
```

# subgraph

```mermaid
graph TD
 subgraph 그룹이름 [표시할 그룹 제목]
	 direction LR
        A --> B
    end
  Mermaid --> Diagram
```