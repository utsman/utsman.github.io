---
layout: post
title: Transaction
category: database
tags: [transaction, database]
---


# Transaction

### ACID 
- A ( Atomicity ) **원자성**
	- 트랜젝션 내의 작업은 모두 성공, 또는 실패해야만 한다.
- C ( Consistency ) **일관성**
	- 무결성 제약 조건을 만족 (pk, fk, not null 등) 하고, 일관성 있는 상태를 유지. 
- I ( Isolation ) **격리성**
	- 여러 트랜젝션이 동시에 일어나더라도, 서로에게 영향을 끼치지 않게 격리.
- D ( Durability ) **지속성**
	- 문제가 발생하였을 때, 성공한 트랜젝션들을 복구 가능해야 한다. ( 로그를 읽어서 재처리 등 )

### 격리 수준
- READ UNCOMMITED
	- 커밋하지 않은 데이타를 읽을 수 있다.
- READ COMMITED
	- 커밋한 데이타만 읽을 수 있다. 반복 조회 시에 데이타가 변경될 수 있다.
- REPEATABLE READ
	- 반복 조회 시에 읽었던 데이타는 달라지지 않지만, 결과 집합의 갯수가 달라질 수 있다. ( Phantom-Read )
- SERIALIZABLE
	- Phantom-Read 가 발생하지 않는다.

