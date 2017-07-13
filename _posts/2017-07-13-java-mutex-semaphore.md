---
layout: post
title: Mutex,Semaphore
category: java
tags: [java, thread, mutex, semaphore]
---


# Mutex,Semaphore

## Mutex 

> 한번에 한 스레드만 특정 락을 소유할 수 있다.
대표적으로 synchronized 가 상호배제 락의 개념을 가지고 있다.



## Semaphore

> 리소스에 액세스할 수 있는 스레드의 갯수를 제한.
갯수가 1개인 경우 binary semaphore, 2개 이상인 경우 counting semaphore 라고 부른다. binary semaphore 의 경우, mutex 와 개념이 같다.
