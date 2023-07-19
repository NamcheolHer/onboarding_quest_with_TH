# AIFFEL Campus Online 5th Code Peer Review Templete

- 코더 : 허남철
- 리뷰어 : 이영빈


# PRT(PeerReviewTemplate)

각 항목을 스스로 확인하고 토의하여 작성한 코드에 적용합니다.

- [x] 1.코드가 정상적으로 동작하고 주어진 문제를 해결했나요?

  코드의 경우 에러없이 작동을 하지만 순서에 상관없이 쌓는 방식으로 되어 있다.

- [x] 2.주석을 보고 작성자의 코드가 이해되었나요?

  작성자 코드가 간결해서 쉽게 이해할 수 있었습니다.

- [x] 3.코드가 에러를 유발할 가능성이 있나요?

  코드가 에러를 유발할 가능성은 없다.

- [x] 4.코드 작성자가 코드를 제대로 이해하고 작성했나요?

  넵 코드 작성자가 코드를 제대로 이해한 상황에서 작성을 진행한걸로 판단됩니다.

- [x] 5.코드가 간결한가요?

  ```python
  def get_score(map_):
      point_table = [0,1,3,5,7,9,11,15,20,25,30,35,40,50,60,70,85,100,150,300]
      counts = [1]
      count = 1
      total_score = 0
      for i in range(19):
          if map_[i] <= map_[i+1]: # 증가
              counts.append(count)
          else: # 작다
              count += 1
              counts.append(count)
  
      for i in range(1,count+1):
          a = counts.count(i)
          b = point_table[a-1]
          print(a, b)
          total_score += b
  
      return total_score # total_score
  ```

  

  

# 참고 링크 및 코드 개선

```python
map_ = ["_" for i in range(20)]
for i in range(20):
    num = int(input())
    map_[i] = num

    print(*map_, sep= "|" )
print("최종점수는 : " ,get_score(map_))


```
