## MONGO DB

  * 데이터베이스 생성  
    * use DB명
  * 컬렉션 생성
    * db.createCollection('컬렉션명')
  * document 생성
    * db.컬렉션명.insertOne({키:값})
    * {키:값} : 도큐먼트

-----
<br>

> 현재 세팅된 데이터베이스 조회 : db  
> 데이터베이스 목록 조회 : show dbs  
> 컬렉션 목록 조회 : show collections
> 컬렉션 데이터 조회 : db.컬렉션명.find()
  
----
<br>

> 데이터베이스 삭제 : db명.dropDatabase()  
> 컬렉션 삭제 : db.컬렉션명.drop()  
> 컬렉션 이름 변경 : db.collection.renameCollection(새이름)  
> 데이터베이스 이름은 변경 불가
