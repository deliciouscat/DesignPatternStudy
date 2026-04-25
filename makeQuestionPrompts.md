`~ Design Pattern`을 학습하기 위한 문제를 하나 내봐. 예를 들어 `조직도 설계` 같은 실전 사례를 서술하면 내가 pseudo code 작성으로 문제를 풀거야. 조직도 문제는 이미 해봤으니 다른 문제로 부탁해.


아래는 Composite Pattern에 대한 문제야. 비슷한 양식으로 만들어줘.

# 문제

**시나리오:**
파일 시스템 탐색기를 만들고 있습니다. 사용자가 파일과 폴더를 트리 구조로 탐색할 수 있어야 하며, 폴더 안에는 다른 폴더와 파일이 모두 포함될 수 있습니다. 또한 전체 저장 공간을 계산하거나 폴더 내 모든 파일을 검색할 수 있어야 합니다.

**요구사항:**
1. 기본 요소: `File` (개별 파일), `Folder` (폴더)
2. 폴더 안에 폴더와 파일을 모두 포함 가능 (중첩 구조)
3. 공통 동작:
   - `getName()`: 이름 반환
   - `getSize()`: 크기 반환 (파일: 파일 크기, 폴더: 내부 모든 파일의 합계)
   - `display()`: 트리 형식으로 계층 구조 출력
   - `search(keyword)`: 이름에 키워드를 포함하는 모든 항목 찾기
   - `delete()`: 파일 또는 폴더 삭제 (폴더는 내용물까지 삭제)

**예시 사용 시나리오:**
```
📁 Projects (root folder)
├─ 📁 DesignPatterns
│  ├─ 📄 composite.py (2.5 KB)
│  ├─ 📄 observer.py (1.8 KB)
│  └─ 📁 tests
│     ├─ 📄 test_composite.py (3.2 KB)
│     └─ 📄 test_observer.py (2.1 KB)
├─ 📁 WebApp
│  ├─ 📄 app.js (15.3 KB)
│  └─ 📁 components
│     ├─ 📄 Button.jsx (0.9 KB)
│     └─ 📄 Modal.jsx (2.5 KB)
└─ 📄 README.md (4.2 KB)

// 사용 예시:
Projects.getSize()  // 전체 크기 계산
Projects.search("composite")  // "composite"를 포함하는 모든 항목 찾기
DesignPatterns.display()  // DesignPatterns 폴더 안의 계층 구조 출력
```

**추가 요구사항:**
- 중복된 이름을 가진 파일/폴더가 같은 폴더 내에 존재할 수 없음
- 같은 객체를 여러 곳에 추가할 수 없음 (복사 관계 아님)
- 폴더 크기는 지연 계산 (lazy evaluation) - 필요할 때만 계산