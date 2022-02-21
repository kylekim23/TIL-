## Mysql 각종 연산자들 
- - - 
## Operators
> 1. __사칙연산__ 
>> select 1 + 2 = 3 출력확인   
select 1 + __'민우'__ =  1이 나온다 문자열을 다 __0__ 으로 인식하기때문
마찬가지로 곱하기 x 나누기 또한 / 동일하게 문자열은 0 으로 인식한다.   
___하지만___ 숫자로 구성된 문자열은 숫자로 자동인식 해준다. 
__예시__ select '1' + '002' * 3  = __7__ 이 출력된다.
- - -
> 2. __컬럼끼리의 더하기도 가능하다.__
>> 단 int형으로 되어있어야 가능   
select orderId, productId, __orderId + productId AS SUM__ from orderDetails
 = >  SUM 컬럼에 아래 쭉 값들 출력됌.
 - - -
> 3. __참/거짓 연산자__ 
>> sql에선 TRUE = __1__, FALSE = __0__ 으로 나타낸다.   
 select !TRUE, NOT 1, !FALSE, NOT FALSE;   
 >>> 1번부터 0, 0, 1 , 1 이 출ㄹ격되는걸 볼 수 있다. 즉   
 __NOT__ , __!__ 는 반대를 뜻함.
 - - -

> 4. __IS, IS NOT__ 연산자 
>> IS : 양쪽이 모두 TRUE 또는 FALSE   
IS NOT : 한쪽은 TRUE, 한쪽은 FALSE
- - -
> 5. __AND, &&__ __OR,||__ 연산자 
>> AND, && : 양쪽이 모두 TURE일때   
OR, || : 어떤 한쪽이라도 TRUE이면 TRUE   
>>> SELECT * FROM OrderDetails
WHERE
  ProductId = 20
  AND (OrderId = 10514 OR Quantity = 50);   
  설명 : 상품번호가 20이면서 상품아이디가 10514d이거나 수량이 50개인 경우의 행을 출력 
- - -
> 6. __비교연산자__ 
>> __=__ : 양쪽 값이 같음 *즉 서버 언어랑은 다르게 =하나로 해결 한다.   
__!=, <>__ : 양쪽 값이 다름   
__>, <__ : (왼쪽, 오른쪽)값이 더 큼 
>>> select productName, price   
__not__ price __>__ 20 as expensive from product   
출력값 : 가격이 20보다 큰 상품의 이름과 가격이 출력 어디에 ? expensive 컬럼에 
- - -
> 7. __BETWEEN {MIN} AND {MAX}__
>> __BETWEEN {MIN} AND {MAX}__ : 두 값 사이에 있음   
__NOT BETWEEN {MIN} AND {MAX}__ : 두 값 사이가 아닌 곳에 있음
>>> SELECT * FROM orderDetails   
WHERE productId BETWEEN 1 AND 4   
출력 : 상품번호가 1~4 인 것들만 출력이 되는것을 볼 수 있다.
- - -
> 8. __IN, NOT IN 연산자__ 
>> SELECT 1 + 2 IN(2,3,4)   
출력 : 1 즉 TRUE를 반환함   
반대로  NOT SELECT 1 + 2 IN(2,3,4) 은 0, FALSE가 출력됌
>>> SELECT * FROM customers WHERE city in ('torino','paris','portland')   
출력 : 해당 도시인 행들만 출력된다. 
- - -
> 9. __LIKE__ 연산자 
>> LIKE '%' : 0~N개 문자를 가진 패턴   
LIKE '_' : _갯수만큼의 문자를 가진 패턴 
>>> SELECT * FROM OrderDetails
WHERE OrderID LIKE '1025_' : 1025로 시작하는 모든 주문번호 출력    
SELECT * FROM Employees
WHERE Notes LIKE '%economics%' : 메모 컬럼에 economics 적혀있는 특정 행들을 출력  
- - -  

## 총정리

* 연산자  의미
> 1. +, -, *, /	
  >> 각각 더하기, 빼기, 곱하기, 나누기
> 2. %, MOD	
  >> 나머지
> 3. IS	
  >> 양쪽이 모두 TRUE 또는 FALSE
> 4. IS NOT	
>> 한쪽은 TRUE, 한쪽은 FALSE
> 5. AND, &&	
>> 양쪽이 모두 TRUE일 때만 TRUE
> 6. OR, ||	
>> 한쪽은 TRUE면 TRUE
> 7. =	
>> 양쪽 값이 같음
> 8. !=, <>	
>> 양쪽 값이 다름
> 9. '>, <	
>> (왼쪽, 오른쪽) 값이 더 큼
> 10. '>=, <=	
>> (왼쪽, 오른쪽) 값이 같거나 더 큼
> 11. BETWEEN {MIN} AND {MAX}	
>> 두 값 사이에 있음
> 12. NOT BETWEEN {MIN} AND {MAX}	
>> 두 값 사이가 아닌 곳에 있음
> 13. IN (...)	
>> 괄호 안의 값들 가운데 있음
> 14. NOT IN (...)	
>> 괄호 안의 값들 가운데 없음
> 15. LIKE '... % ...'	
>> 0~N개 문자를 가진 패턴
> 16. LIKE '... _ ...'	
>> _ 갯수만큼의 문자를 가진 패턴