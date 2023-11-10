1. NFC 리더 및 라즈베리 파이 설정: NFC 리더를 라즈베리 파이에 연결하고, 라즈베리 파이에서 NFC 카드의 정보를 읽기 위한 설정

2. Node.js 및 MariaDB 연결 설정: 라즈베리 파이에서 Node.js를 사용하여 MariaDB와 연결하고, 데이터를 삽입할 수 있는 연결을 설정 ``` pip install mysql``` 

3. NFC 데이터 MariaDB로 전송: NFC 카드의 고유번호를 읽은 후, Node.js 애플리케이션을 사용하여 MariaDB로 해당 데이터 전송 라즈베리파이에서 Node.js 실행

4. HTML 파일 생성: MariaDB에서 데이터를 추출하고, 해당 데이터를 HTML 파일로 출력할 수 있도록 HTML 파일을 생성합니다. 
``` 데이터를 표 형태로 추출하는게 우선```

5. 라즈베리 파이와 Node.js 설정: 라즈베리 파이에서 Node.js 애플리케이션을 실행하여 MariaDB로부터 데이터를 가져와 HTML 파일에 삽입

6. 웹 서버 구축 및 HTML 파일 렌더링: 라즈베리 파이에서 Express 모듈을 사용하여 웹 서버를 구축, HTML 파일을 렌더링하여 데이터를 표시