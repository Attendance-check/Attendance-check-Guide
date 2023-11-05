## MariaDB 

### PN532 module library
libnfc & pynfc

### MariaDB library Setting
mysql-connector-python

### 고유 코드 DB에 넣는 python code

### Example Code
``` import mysql.connector
import PN532  # PN532 라이브러리 임포트

# MariaDB 연결 설정
mydb = mysql.connector.connect(
  host="localhost",
  user="yourusername",
  password="yourpassword",
  database="yourdatabase"
)
mycursor = mydb.cursor()

# PN532 모듈 초기화
pn532 = PN532.PN532()
pn532.begin()
ic, ver, rev, support = pn532.get_firmware_version()

# NFC 카드 값 읽기
uid = pn532.read_passive_target()
if uid is not None:
    # MariaDB에 값 삽입
    sql = "INSERT INTO yourtable (uid) VALUES (%s)"
    val = (uid,)
    mycursor.execute(sql, val)
    mydb.commit()
    print(mycursor.rowcount, "record inserted.")

# MariaDB 연결 닫기
mydb.close()
```