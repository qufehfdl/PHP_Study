2023.04.18 PHP 공부 시작!
 - 서버 사이드 스크립트 (서버 측의 기술) 언어!<br>
   서버측 기술은 크게 세가지!
   1. Apache , nginX , IIS ...
   2. PHP , Python , JAVA ...
   3. MySQL , Oracle ...
 - HTTP 프로토콜과 마찬가지로 상태를 유지하지 않는 특성

 - PHP에서 MySQL DB에 연결하는 방법으로는<br>
   MySQLi  ,  PDO 방식이 있다



// 결과 값에서 특정 컬럼에 mb_convert_encoding() 함수 적용
while($row = mysqli_fetch_array($result)) {
    $specific_column = $row['specific_column'];
    $specific_column = mb_convert_encoding($specific_column, 'UTF-8', 'CP949'); // cp949 -> utf-8 로 변환
    $row['specific_column'] = $specific_column; // 변환된 값으로 업데이트
}


하지만, PHP 5.5.0 이후로는 iconv를 사용하지 않는 것이 좋으며, 'mb_convert_encoding' 함수를 사용하는 것을 권장합니다.
