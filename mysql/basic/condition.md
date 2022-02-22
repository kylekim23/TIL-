# 조건에 따라 그룹으로 묶기
- - -
> 1. __GROUP BY__  - 조건에 따라 집계된 값을 가져옵니다.
>> 예시 : SELECT Country FROM Customers   
__GORUP BY__ Country;   
출력값 : 같은 국가끼리 묶은 겹치지않은 값들이 나오게 된다.   
두번째 예시 : 여러 컬럼을 기준으로 그룹화   
SELECT Country, City, CONCAT_WS(',', City, Country)   
FROM Customers   
__GROUP BY__ Country, City;   
출력값 : 국가와, 도시가 겹치지않은 값들이 나오게된다.
> 2. __GROUP BY와 COUNT의 조합__
>> 예시 : SELECT COUNT(*), OrderDate   
FROM Orders   
GROUP BY OrderDate;   
출력값 : 날짜를 기준으로 묶은다음에 그 날짜마다의 갯수를 나타내준다. 즉 해당하는 날짜에 몇개의 주문이 있었는지 확인이 가능하다.