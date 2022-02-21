# 숫자와 문자열을 다루는 함수들 
- - - 
## 숫자 관련 함수들
> 1. __ROUND, CEIL, FLOOR__ 
>> ROUND : 반올림    
CEIL : 올림   
FLOOR : 내림 
>>> 예시 : SELECT ROUND(0.5), CEIL(0.4), FLOOR(0.6);   
출력값 : 1, 1, 0 
> 2. __ABS 절대값__ 
>> 예시 : SELECT ABS(1), ABS(-1), ABS(3 -10);
>>> 출력값 : 1, 1, 7
> 3. __GREATEST, LEAST__ 
>> GREATEST : __(괄호)__ 안에서 가장 큰 값   
LEAST : __(괄호)__ 안에서 가장 작은 값 
>>> 예시 : GREATEST(1,2,3), LEAST(1,2,3,4,5);   
출력 : 3, 1 
> 4. 그룹 함수 
>> __MAX__ : 가장 큰 값, MIN : 가장 작은값    
__COUNT__ : 갯수(NULL값 제외),   
__SUM__ : 총합, AVG : 평균값
>>> 예시 : SELECT MAX(QUANTITY), MIN(QUANTITY),COUNT(QUANTITY),   
SUM(QUANTITY), AVG(QUANTITY) FROM OrderDetails;  
> 5. 제곱 함수
>> __POW(A, B), POWER(A, B)__ : A를 B만큼 제곱   
__SQRT__ : 제곱근 
>>> 예제 : SELECT POW(2,3), POWER(5,2), SQRT(16);   
출력값 : 8, 25, 4
> 6. __TRUNCATE(N, n)__ : N을 소숫점 n자리까지 선택 
>> 예시 : SELECT price FROM Products   
WHERE TRUNCATE(price, 0) = 12;   
출력값 : 상품가격중 소수점 0까지 잘랐을때 12로 시작하는것을 출력한다   12, 12.05, 12.23 
- - -
## 문자열 관련 함수들 
> 1. __UCASE, UPPER__ : 모두 대문자로, LCASE, LOWER : 모두 소문자로   
>> 예시 :  UPPER('aBc'), LOWER('AbC')   
출력값 : ABC, abc  이처럼 전부 대문자 또는 소문자로 바꿔버린다.
> 2. __CONCAT( )__ : 괄호 안의 내용 이어붙임,   
CONCAT_WS(s..) : 괄호 안의 내용 S로 이어붙임
>> 예시 : SELECT CONCAT('HELLO','','THIS IS', 2022)   
SELECT CONCAT_WS('-','2022, 2, 21, 'PM');   
출력값 :  HELLO THIS IS 2022, 2022-2-21-PM   
모든 값을 __문자열__ 로 바꿔버린다 이점 유의하자.
> 3. __SUBSTR, SUBSTRING, LEFT, RIGHT__
>> SUBSTR, SUBSTRING : 주어진 값에 따라 문자열 자름    
LEFT : 왼쪽부터 N글자, RIGHT : 오른쭉부터 N글자 
>>> 예시 : SELECT   
  SUBSTR('ABCDEFG', 3),   
  SUBSTR('ABCDEFG', 3, 2),   
  SUBSTR('ABCDEFG', -4),   
  SUBSTR('ABCDEFG', -4, 2);   
  SELECT   
  LEFT('ABCDEFG', 3),   왼쪽부터 3번째까지
  RIGHT('ABCDEFG', 3);   오른쪽부터 3번째까지 
  출력값 : CDEFG, CD, DEFG, DE   
  출력값 : ABC, EFG  
  >>>> 실생활 예시 : SELECT OrderDate,   --> __1998-03-23__
  LEFT(OrderDate, 4) AS Year,   
  SUBSTR(OrderDate, 6, 2) AS Month,   
  RIGHT(OrderDate, 2) AS Day   
  FROM Orders;   
출력값 : YEAR : 1998 MONTH : 03 DAY : 23 



  