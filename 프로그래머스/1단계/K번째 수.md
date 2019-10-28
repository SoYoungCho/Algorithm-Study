![image](https://user-images.githubusercontent.com/38921656/67681014-d3e41f00-f9cf-11e9-9d66-bb30289cb508.png)
![image](https://user-images.githubusercontent.com/38921656/67680779-53bdb980-f9cf-11e9-9cc3-ca23adc3c1a7.png)

## 나의 풀이

```python
def solution(array, commands):
    answer = []
    for command in commands:
        i,j,k = command
        answer.append(sorted(array[i-1:j])[k-1])
    return answer

solution( [1, 5, 2, 6, 3, 7, 4],[[2, 5, 3], [4, 4, 1], [1, 7, 3]]) # [5,6,3]
```

## 모범답안

```python
def solution(array, commands):
    return list(map(lambda x:sorted(array[x[0]-1:x[1]])[x[2]-1], commands))
```

파이썬 풀이 중 가장 좋아요를 많이 받은 풀이이다.
