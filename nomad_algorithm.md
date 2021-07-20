# 1. Array ⟶ Reading 👍

Array의 오퍼레이션 [ Read, Search, Add, Delete ]

- **Time Complexity (시간복잡도)**
  : 데이터 구조의 오퍼레이션 혹은 알고리즘이 얼마나 빠르고 느린지 측정하는 방법
  얼마나 많은 '단계'가 있는가로 측정

2종류의 메모리가 있다

1. `volatile memory (휘발성 메모리)`: memory RAM (Random Access Memory)
2. `non-volatile memory (비휘발성 메모리)` : Hard Drive

프로그램이 돌아가고 변수생성할 때 RAM에 저장(메모리가 하드드라이브보다 빠름)

---

> 오퍼레이션

1. `Reading` : 빠름 👍
   array는 0부터 인덱싱을 한다, 많은 자료를 읽어야 한다면 array가 유용함
   (랜덤엑세스로 빠르게 접근 가능)

2. `Searching` -> `Linear Search` (선형검색): 별로 안 빠름 👎
   찾는 값이 배열에 있는지 없는지 모름, 위치도 모름
   (array는 랜덤엑세스가 있어서 쉽게 접근할 수 있지만 하나하나 다 확인해야함)

3. `Insert` (Add , write) :
   3가지 가능성이 있음, 배열을 만들 때는 크기를 미리 알려줘서 메모리 공간을 확보해야함

   - ①: 배열의 맨 끝에 추가하는 경우 👍
   - ②: 배열의 중간에 추가하는 경우, soso 🤏
   - ③: 배열의 맨 앞에 추가하는 경우 👎 (배열의 모든 아이템을 뒤로 옮겨야함)
   - 👎: 이미 배열의 공간이 꽉 차있는데 값을 추가해야하는 경우

4. `Delete` add와 비슷함
   - ①: 배열의 맨 끝을 삭제하는 경우 👍 (인덱스가 있기땜에 그냥 가서 지우면 끝)
   - ②: 배열의 중간을 삭제하는 경우, soso 🤏 (삭제된 아이템의 공백을 채우기 위해 뒤의 아이템들이 움직임)
   - ③: 배열의 맨 앞을 삭제하는 경우 👎 (배열의 모든 아이템을 뒤로 옮겨야함)

---

# 2. 검색 알고리즘 Search Algorithm

`① Linear Search (선형검색 알고리즘)`
: 맨앞부터 순서대로 차근차근 검색
if 찾는 값이 맨뒤에 있거나, 없으면 ? 👎

- linear time complexity, 선형 시간복잡도
  : input 이 많을 수록 time도 선형적으로 증가

`② Binary Search (이진검색)`
: _Sorted Array_(정렬된 배열)에만 사용 가능

하지만!
*sorted array*에 아이템을 `추가`하는 건 정렬이 안된 일반 배열에 추가하는 것보다 시간이 걸림
(일반 배열은 맨뒤에 끼워넣으면 끝)
정렬된 배열에서 `검색`은 훨씬 빠름

🤔
Array에서 검색을 많이 하는 상황? ⟶ sorted array가 유용함
But, sorted array에서 아이템 추가할 땐? ⟶ 시간이 걸린다

---

# 3. Big O

- O(n) ⟶ ex, linear (2n이어도 똑같음)
- O(1) ⟶ 항상 특정한 값의 스텝이 필요하다면 (Constant time)
- O(n²) ⟶ Quadratic time
- O(log n) ⟶ binary search 이진검색의 시간복잡도

`Quadratic Time (2차 시간)`
: Nested Loops, 중첩반복이 있을 때 발생함

`Logarithmic Time (로그 시간)`
: 이진검색 알고리즘 설명할 때 사용

exponet (지수) ⟷ logarithm (로그)

---

# 4. Sorting Algorithm

- `① Bubble Sort 버블정렬` ⟶ O(n²)
  : 자주 사용되진 않음, 배열의 두 아이템을 선택하고 비교해서 정렬 👎

- `② Selection Sort 선택정렬` ⟶ O(n²)
  : 모든 아이템을 스캔 🤏

- `③ Insertion Sort 삽입정렬` ⟶ O(n²)
  : 필요한 아이템을 스캔 👍 (sorting 알고리즘 내에서 그나마 나은 것)
  best 시나리오에서 O(n) 이 발생함

삽입, 선택 정렬은 작은 데이터를 이용할 땐 👍
