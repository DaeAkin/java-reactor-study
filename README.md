## 🧐 Reactor ? RxJava ? 뭐가 다르지 ? 

### Reactor

**Reactor** 는 JVM에서 돌아가는 <u>non-blocking</u> 애플리케이션을 만들 때 사용하는 라이브러리 입니다. [Reactive Streams 스펙](https://www.reactive-streams.org/)을 기반으로 JVM에서 non-blokcing 애플리케이션을 만들기 위한 4 세대 Reactive 라이브러리 입니다. 효과적인 처리를 위해 non-blokcing 개념을 사용했으며, Java의 Functional API, Completable Future, Stream, Duration 등 API와 상호작용 합니다. 

**그와 반대로, RxJava**는 Reactive의 확장팩 입니다. 비동기와 이벤트 기반 프로그램을 지원하는 라이브러리 입니다.

Reactor는 마이크로서비스 아키텍처, Reactor Netty 등 HTTP , TCP UDP을 기반으로 돌아가는 네트워크에서 backpressure(배압조절) 이라는 기능을 지원합니다.

Reactor는 Java 8 이상을 지원합니다.

### Why

Reactive Programming is a new paradigm in which you use *declarative code* (in a manner that is similar to *functional programming*) in order to build asynchronous processing pipelines. It is an event-based model where data is pushed to the consumer, as it becomes available: we deal with asynchronous sequences of events.

This is important in order to be more efficient with resources and increase an application's capacity to serve large number of clients, without the headache of writing low-level concurrent or and/or parallelized code.

By being built around the core pillars of being fully **asynchronous** and **non-blocking**, Reactive Programming is an alternative to the more limited ways of doing asynchronous code in the JDK: namely *Callback* based APIs and `Future`.

It also facilitates composition, which in turn makes asynchronous code more readable and maintainable.

### Reactive Streams

The **Reactive Streams** specification is an industry-driven effort to standardize Reactive Programming libraries on the JVM, and more importantly specify how they must behave so that they are interoperable. Implementors include Reactor 3 but also RxJava 2, Akka Streams, Vert.x and Ratpack.

It contains 4 very simple interfaces as well as a TCK, which shouldn't be overlooked since it is the rules of the specification that bring the most value to it.

From a user perspective however, it is fairly low-level. Reactor 3 aims at offering an higher level API that can be leverage in a large breadth of situations, building it on top of Reactive Streams `Publisher`.





## 참고자료

https://projectreactor.io/docs/core/release/reference/