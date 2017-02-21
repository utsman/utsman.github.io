---
layout: post
title: Java 의 lambda
category: java
tags: [java, lambda]
---

> 람다는 익명 메서드라고 말할 수 있다.

> 람다 표현식은 메서드로 전달할 수 있는 익명 함수를 단순화한 것이라고 할 수 있다.

#### 람다의 특징

- **익명**

	 보통의 메서드와 달리 이름이 없으므로 익명이라 표현한다.
- **함수**

	 람다는 메서드처럼 특정 클래스에 종속되지 않으므로 함수라고 부른다. 하지만 메서드처럼 파라미터 리스트, 바디, 반환 형식, 가능한 예외 리스트를 포함한다.
- **전달**

	 람다 표현식을 메서드 인수로 전달하거나 변수로 저장할 수 있다.
- **간결성**


#### 람다를 사용한 예제

```java
// 기존 코드
Comparator<String> comparator = new Comparator<String>() {
	@Override
		public int compare(String o1, String o2) {
		return o1.compareTo(o2);
	}
};

// 람다를 사용한 코드
Comparator<String> comparator = (a, b) -> a.compareTo(b);

// 람다 없이, java 8 에서는 아래와 같이도 가능하다.
Comparator<String> comparator = Comparator.naturalOrder();
```

#### 어디에 람다를 사용할 수 있을까?

> 하나의 메서드만 선언된 인터페이스만을 람다로 표현할 수 있다.

#### @FunctionalInterface
- interface 에 1개의 메소드만 선언.
- 그러나 Consumer 클래스를 까보면, 메소드가 2개이다. 그러나 다른 1 개의 메소드는  default 로 선언되었기 때문에..

#### 람다가 자바에서 동작하는 원리

#### 참고
[http://jdm.kr/blog/181](http://jdm.kr/blog/181)

[http://www.xenomity.com/entry/Java-8-Lambda-Expression%EA%B3%BC-%EB%B3%80%EA%B2%BD%EB%90%9C-Interface%EC%9D%98-%EB%AA%A8%ED%98%B8%ED%95%A8](http://www.xenomity.com/entry/Java-8-Lambda-Expression%EA%B3%BC-%EB%B3%80%EA%B2%BD%EB%90%9C-Interface%EC%9D%98-%EB%AA%A8%ED%98%B8%ED%95%A8)



