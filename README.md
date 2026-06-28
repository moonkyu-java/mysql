필기 1일차!


데이터 베이스는 데이터를 표 형태 저장한다

열이 세로 행이 가로 데이터베이스에서는 행은 제목 생략함

표를 모아논게 데이터 베이스


데이터 베이스에 설계도는 스키마


스키마들을 모아논게 데이터 베이스 서버

2일차!
-- 1. 작업할 데이터베이스 폴더로 들어가는 코드

-USE opentutorials;

-- 2. topic 이라는 이름의 새로운 표를 만드는 시작 코드

-CREATE TABLE topic(

-- 3. 순번 기둥 설정: 정수만 허용, 빈칸 금지, 번호 자동 생성 옵션 INT옆에 숫자 11은 최소 칸수 예를 들면

- [_][_][_][_][_][_][_][_][1][2][3]  <-- 총 11칸을 맞춰서 출력함
- 
- [1][2][3][4][5][6][7][8][9][0][1][2][3]  <-- 잘리지 않고 13자리 다 출력됨
- 
-id INT(11) NOT NULL AUTO_INCREMENT,


데이터 베이스 선택 밑에서 opentutorials가 내가 만든 데이터 베이스 이름
 USE opentutorials; 


위에 만들고 선택한 데이터 베이스 opentutorials에 topic라는 테이블(표)를 생성 

NOT NULL사용하면 그 공간에 공백 불가

PRIMARY KEY(id)); 칸을 중복이 절대 없는 주민등록번호(대표 식별자)로 지정

 CREATE TABLE topic(
 
    -> id INT(11) NOT NULL AUTO_INCREMENT,
    
    -> title VARCHAR(100) NOT NULL,
    
    -> created DATETIME NOT NULL,
    
    -> author VARCHAR(30) NULL,
    
    -> profile VARCHAR(100) NULL,
    
    -> PRIMARY KEY(id));

테이블 확인하기

    DESC topic;

테이블에 데이터 넣기 새로운 행 추가할때 사용 칸 갯수와 데이터값 개수 일치해야함

    INSERT INTO topic (title, description, created, author, profile) 
    
VALUES ('MySQL', 'MySQL is...', NOW(), 'egoing', 'developer');

추가하고 테이블안에 데이터 확인할때 

SELECT * FROM topic;



    
