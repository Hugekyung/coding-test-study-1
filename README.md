# 알고리즘 문제풀이

## 풀이 목록

<<<<<<< HEAD
|  #  |   날짜   |           문제이름           |                               링크                               |                                                                          풀이                                                                          | 완료 |  Best  |
| :-: | :------: | :--------------------------: | :--------------------------------------------------------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------: | :--: | :----: |
|  1  | 22-01-20 |           단어정렬           |           [문제](https://www.acmicpc.net/problem/1181)           | [단어정렬.md](https://kdt-gitlab.elice.io/eunhyekim1223/codingtest-study/-/blob/master/GwangCheon/BOJ-1187/%EB%8B%A8%EC%96%B4%20%EC%A0%95%EB%A0%AC.md) |  ✔   | 신광천 |
|  2  | 22-01-25 |             로프             |           [문제](https://www.acmicpc.net/problem/2217)           |                                                                                                                                                        |  ❌  |        |
|  3  | 22-01-25 |        전쟁-땅따먹기         |           [문제](https://www.acmicpc.net/problem/1270)           |                                                                                                                                                        |  ❌  |        |
|  4  | 22-01-25 |           폴짝폴짝           |           [문제](https://www.acmicpc.net/problem/1326)           |                                                                                                                                                        |  ❌  |        |
|  5  | 22-01-25 |          수열의 합           |           [문제](https://www.acmicpc.net/problem/1024)           |                                                                                                                                                        |  ❌  |        |
|  6  | 22-01-25 | Fly me to the Alpha Centauri |           [문제](https://www.acmicpc.net/problem/1011)           |                                                                                                                                                        |  ❌  |        |
|  7  | 22-01-29 |          단어 변환           | [문제](https://programmers.co.kr/learn/courses/30/lessons/43163) |                                                                                                                                                        |  ❌  |        |
|  8  | 22-01-29 |             카펫             | [문제](https://programmers.co.kr/learn/courses/30/lessons/42842) |                                                                                                                                                        |  ❌  |        |
|  9  | 22-01-29 |            후보키            | [문제](https://programmers.co.kr/learn/courses/30/lessons/42890) |                                                                                                                                                        |  ❌  |        |
| 10  | 22-01-29 |         최소직사각형         | [문제](https://programmers.co.kr/learn/courses/30/lessons/86491) |                                                                                                                                                        |  ❌  |        |
=======
| # | 날짜 | 문제이름 | 링크 | 풀이 | 완료 | Best |
| :---: | :---: | :---: | :---: | :---: | :---:| :---: |
| 1 | 22-01-20 |단어정렬 | [문제](https://www.acmicpc.net/problem/1181) |[단어정렬.md](https://kdt-gitlab.elice.io/eunhyekim1223/codingtest-study/-/blob/master/GwangCheon/BOJ-1187/%EB%8B%A8%EC%96%B4%20%EC%A0%95%EB%A0%AC.md) | ✔ | 신광천 |
| 2 | 22-01-25 | 로프 | [문제](https://www.acmicpc.net/problem/2217) | | ❌| |
| 3 | 22-01-25 | 전쟁-땅따먹기 | [문제](https://www.acmicpc.net/problem/1270) | | ❌| |
| 4 | 22-01-25 | 폴짝폴짝 | [문제](https://www.acmicpc.net/problem/1326) | | ❌| |
| 5 | 22-01-25 | 수열의 합 | [문제](https://www.acmicpc.net/problem/1024) | | ❌| |
| 6 | 22-01-25 | Fly me to the Alpha Centauri | [문제](https://www.acmicpc.net/problem/1011) | | ❌| |

## Tips
 - **from collections import defaultdict**
    - dict\[i\] += 1 (초기화 없이 사용가능)
 
 - **for-else, while-else 구문**
   ```python
   for or while:  
      블라블라  
      break  
   else:
   # break를 통해 루프가 끝나지 않았을 경우에 쓰는 코드
   ```  
      
 - **BFS: 큐를 이용 (from collections import deque)**
    - 최단거리 문제 (DFS보다 빠를때가 많음)
 - **DFS: 스택를 이용 (python list 사용)**
    - 백트래킹 문제 (모든 경우의 수를 봐야할 때)
 - **import sys**
    - ``sys.setrecursionlimit(limit_number)``
      - 재귀함수 제한 해제하고 싶을 때 ( default = 1000 )
    - ``sys.stdin.readline()``
      - 입력 받을 때 ( input 보다 속도상에서 우위, 문자열로 입력받을 때 \n 개행까지 입력받으므로 주의 )
>>>>>>> 8a992aee9ce46120ad226d4cda8aa4e363edfa76
