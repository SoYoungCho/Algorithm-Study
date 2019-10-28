![image](https://user-images.githubusercontent.com/38921656/67682710-502c3180-f9d3-11e9-8538-97ddb106f558.png)
![image](https://user-images.githubusercontent.com/38921656/67682736-5f12e400-f9d3-11e9-9f05-0ec5a90d8562.png)

## 나의 풀이 (첫 도전)

```python
def solution(s):
    answer = True
    numP = 0
    numY = 0
    
    for char in s:
        if char == 'p' or char == 'P':
            numP += 1
        elif char == 'y' or char == 'Y':
            numY += 1
    
    if numP == numY or numP == 0 and numY == 0:
        answer = True
    elif numP != numY:
        answer = False
    
    return answer

solution("pYY") #False
```

위 풀이는 단순히 하나씩 확인하여 세는 것인데, 비효율적인 것 같아 고민하다가 아래와 같이 다시 풀었다.
다시 푼 풀이가 좋아요를 가장 많이 받은 풀이여서 기분이 좋았다!

## 나의 두 번째 풀이 (모범답안)

```python
def solution(s):
    return s.upper().count('P') == s.upper().count('Y')

solution("pYY") # False
```

알파벳을 대문자로 바꾸어주는 upper() 와 카운팅해주는 count()를 사용하였다.
(lower() 사용 가능)

