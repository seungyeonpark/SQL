# SQL

## Programmers
### Group by
- 쿼리문의 실행 순서
    - 쿼리문의 실행 순서
        ```
        FROM/JOIN → WHERE → GROUP BY → HAVING → SELECT → DISTINCT → ORDER BY → LIMIT/OFFSET
        ```
    - HAVING은 GROUP BY 이후 적용되므로 그룹화되어 나온 결과에 조건식이 적용된다
        ``` SQL
        SELECT ANIMAL_TYPE, COUNT(ANIMAL_TYPE)
        FROM ANIMAL_INS 
        GROUP BY ANIMAL_TYPE 
        ORDER BY ANIMAL_TYPE;
        ```
### Is null
- NVL
    - NVL(expr1, expr2)
        - expr1의 값이 null인 경우 expr2 값으로 반환
    - NVL2(expr, expr1, expr2)
        - expr의 값이 null이 아닐 경우에는 expr1의 값을 반환하고, null인 경우에는 expr2의 값을 반환
### Sum, Max, Min
- COUNT(DISTINCT 컬럼)
    - 컬럼 값의 중복을 제거하고, 컬럼 값 건수를 반환
