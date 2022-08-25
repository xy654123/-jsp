# DB 연결
![image](https://user-images.githubusercontent.com/96267331/186085054-c46a4939-53c2-4028-b85c-f88637f3381a.png)<br>\
다음코드는 DB와 자바파일을 연결시켜주는 코드인데 문자열의 id pw url 값을 적어주고 try catch 문을 이용하여 예외처리를 하게된다 예외처리는 예외상황일때 오류로 뜨는것을 막아준다Connection객체를 이용하여 DB와 연결 시켜 준다

# 테이블
![image](https://user-images.githubusercontent.com/96267331/186085513-12914ea8-d279-44c2-a6dd-2b9dcf675e3a.png)
![image](https://user-images.githubusercontent.com/96267331/186085591-e5449e8e-4dd1-4dd2-b0e3-cfe25cfd49bf.png)<br>
위에 sql문은 테이블을 생성해주고 값을 넣어주는 과정이다 테이블을 생성할때는 컴럼id와 형태(값)을 입력하여 생성해주며 값을 넣을때는
생성한 테이블형태와 조건에 맞게 순서대로 입력해주어야 한다

# join 화면

![image](https://user-images.githubusercontent.com/96267331/186064795-fefcda23-bba1-4d40-83aa-b8d9c929934b.png)

# join 코드
![image](https://user-images.githubusercontent.com/96267331/186065528-b0393790-46d0-441d-bbb9-bb57811036e8.png)<br>
테이블 첫번째 줄의 값은 자동으로 발생되는데 밑에 코드가 바로 자동으로 값을 넣어주는 작업이다
![image](https://user-images.githubusercontent.com/96267331/186065415-b5d331e1-b334-4601-bc43-1615de020801.png)<br>
sql 이라는 문자열에 쿼리문을 작성하여 넣어주고 conn을 통해 DB와 연결 해준다 PreparedStatement 통해
서 정적 쿼리문을 DB로 전달해준다 그리고 그 값을 넣어준 변수 pstmt를 이용하여 쿼리의 결과를 담는
객체인 ResultSet을 통하여 rs 값을 받은후 rs를 사용하여 num에게 쿼리문 결과에 +1 한값을 넣어 회원번호를 만들어 출력해준다<br>
![image](https://user-images.githubusercontent.com/96267331/186083513-b456dc0e-d215-4469-8f82-13058b08d24f.png)<br>
다음 코드는 자바스크립트 코드인데 이코드는 checkValue 라는 함수를 만들어 사용한다 이 함수에서는 폼 문에있는 버튼을 눌렀을때 사용되며 if문을 통해서
!document.data.name.value라는 것을 이용하여 input에 value 값이 있는지 없는지를 검사해주는것이다 만약 있다면
계속 넘어가 true에 도달하게 되지만 값이 없다면 알림을 통해 알려주고 false값을 줘 다시 입력할수있게 만드는 코드이다<br>
![image](https://user-images.githubusercontent.com/96267331/186084371-a3ea3263-c3db-474e-91e3-2766bcc848a2.png)<br>
join파일에 마지막 코드이다 form문안에 테이블문을 넣어서 그 테이블속에 input값을넣어줘 화면의 모양을 만들어주는 코드이다

# join_p 
![image](https://user-images.githubusercontent.com/96267331/186321591-23e1924a-f426-4d47-aa88-67df41184b8a.png)<br>
다음 코드는 join에서 form 문에 있던 action에 사용되는 코드이다 첫번째 줄에있는 코드는 UTF-8로 변환해주는 코드이며 한글 화면이 꺠지는 것을 방지해준다
문자열인 sql 쿼리문을 저장시켜주고 conn를 통해 DB 자바와 연결시켜 준다 pstmt를 통해 쿼리문을 DB로 전달시켜 준다 그다음줄부터는 sql 문자열에서 ?에 값을 넣주는것인데 모두 문자열로 입력받게된다 하지만 첫번째줄에있는 값은 int 값으로 받아줘야되기 때문에 Intger.parseInt로 변화하여 값을 넣어준다 그다음 마지막 줄 코드를 실행시켜 DB를 업데이트 시켜준다<br>
# 테이블 값 변화
![image](https://user-images.githubusercontent.com/96267331/186092000-751a7831-f00e-45b3-9ec1-1d74e22962a0.png)<br>
![image](https://user-images.githubusercontent.com/96267331/186094092-d5c923ee-4cf0-42b8-874c-0de368c87acb.png)<br>
![image](https://user-images.githubusercontent.com/96267331/186094223-23b32810-d3db-455d-9beb-c389d4d6aec8.png)

# member_list 화면
![image](https://user-images.githubusercontent.com/96267331/186558603-17d75313-e10f-4b14-80ad-d331961b47a6.png)

# member_list 코드 설명
![image](https://user-images.githubusercontent.com/96267331/186558765-78117691-0c12-416b-b90a-c8a9cd949c4a.png)<br>
이 코드는 문자열인 sql 쿼리문을 작성해주는것이다 쿼리문의 내용은 member_tbl_02를 오름차순으로 정렬을 하고 테이블에 custno, custname, phone, address, joindate는 
검색해주는데 yyyy-mm-dd 형식으로 to_char을 이용해 바꾸어 주면 컬럼명이 이상하게 바뀌었기 때문에
joindate 라는 별칭으로 바꾸어준다 그다음 grade 검색할때는 case 통해 조건을걸고 그 조건의 맞을때 나올값을
설명해준는 것이다 grade 가 A 일때는 VIP B 일때는 일반 나머지는 직원으로 나오게 설명한뒤 end를 써
작업을 끝내주고 grade 라는 별칭을 준다 그리고 city를 마지막으로 검색해주는 쿼리문을 작성한것이다<br>
![image](https://user-images.githubusercontent.com/96267331/186561419-224acf12-1bcb-4bb8-a58b-031e12250806.png)<br>
Connection 객체를 통해서 DB와 연결 시켜준후 방금 작성한 sql 쿼리문을 PreparedStatement로 전달시켜준다 그리고 그 결과 값을 ResultSet 통해 rs의 값을 넣어준다<br>
![image](https://user-images.githubusercontent.com/96267331/186562001-be54806b-fa8e-4bd8-97d3-e08f7ce29113.png)<br>
다음코드에서 테이블의 첫줄 헤드 라인의 값을 넣어주고 왼족의 버튼을 추가해준다 그리고 테이블 안에 있는 값은 while문에 조건을 rs.next()로 넣어줘 마지막 행까지 반복을 시켜 그 안에
있는 결과값이 들어있는 rs가 문자열 상태로 저장되어있어 getString로 테이블의 값을 넣어준다

