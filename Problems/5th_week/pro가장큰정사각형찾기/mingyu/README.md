풀이
====
접근 방법
----------------------
* 2*2 크기의 정사각형을 만들어 계속 검사했습니다.
* 이 때 기준점을 우측 하단의 인덱스로 잡아 좌측, 상단, 좌상단의 값들을 확인하면서 해당 값 중 가장 작은 값에+1을 하여 기준점을 업데이트 합니다.
* 해당 작업을 반복하면 
  [[0,1,1,1],
   [1,1,1,1],
   [1,1,1,1],
   [0,0,1,0]]의 경우

  [[0,1,1,1],
   [1,1,2,1],
   [1,2,1,3],
   [0,0,1,0]]가 됩니다.

* 이를 chain을 통해 하나의 리스트로 묶어준 후 가장 큰 값을 제곱해줌으로써 가장 큰 정사각형의 크기를 구할 수 있습니다.

어려웠던 부분
----------------------
* 처음에는 이중배열로 접근하려다 효율성이 망가지는 바람에 새로운 방법을 찾아야 했습니다.
* 가로 세로의 최대 길이를 구하는 방법만 생각나서 해당 dp형식으로 푸는 방법은 인터넷을 찾아보게 되었습니다.

새로 알게 된 것
----------------------
* itertools.chain.from_iterable()
