# Mysql 베이직
- - -
## SELECT 
> 1. 해당 테이블 정보 출력 
  >> select * from OrderDetials
> 2. 해당 테이블 특정 컬럼 출력 
  >> select __OrderId__ from OrderDetails
> 3. 해당 테이블 특정 조건에 해당하는 행들 출력
  >> select * from OrderDetails   
  where Quantity < 5   
> 4. 원하는 순서대로 데이터 가져오기 
  >> select * from customers   
  __order by__ contactName;  ___asc___ = 오름차순 
  ___desc___ = 내림차순 
>5. 원하는 만큼만 데이터 가져오기 
  >> select * from customers __limit__ 10; 10개데이터   
  또는 limit{건너뛸 갯수 } , {가져올 갯수 }를 사용하여, 원하는 위치에서 원하는 만큼만 데이터를 가져올 수 있다.   
  select * from customers __limit__10, 30  --> 10번부터 30개의 데이터를 가져오겠다. 
>6. 원하는 별명(alias)으로 데이터 가져오기 
  >> AS를 사용해서 컬럼명을 변경할 수 있다.   
  select cusmoerId __as__ ID,   
  customerName __as__ Name from customers
>7. 오늘 배운것을 모두 이용해보기 
      >> SELECT
      CustomerID AS '아이디',
      CustomerName AS '고객명',
      City AS '도시',
      Country AS '국가'
    FROM Customers
    WHERE
      City = 'London' OR Country = 'Mexico'
    ORDER BY CustomerName
    LIMIT 0, 5;