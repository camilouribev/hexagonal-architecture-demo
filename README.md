# hexagonal-architecture-demo

Ejemplo de propuesta genérica para implementar una arquitectura hexagonal. La estructura de paquetes es la siguiente:


├── build.gradle
├── gradle
│   └── wrapper
│       ├── gradle-wrapper.jar
│       └── gradle-wrapper.properties
├── gradlew
├── gradlew.bat
├── HELP.md
├── settings.gradle
└── src
    ├── main
    │   ├── java
    │   │   ├── com
    │   │   │   └── example
    │   │   │       └── hexagonaldemo
    │   │   │           └── HexagonaldemoApplication.java
    │   │   ├── domain
    │   │   │   ├── commands
    │   │   │   │   ├── AddProduct.java
    │   │   │   │   ├── DeleteProduct.java
    │   │   │   │   └── UpdateProduct.java
    │   │   │   ├── entities
    │   │   │   │   └── Product.java
    │   │   │   ├── events
    │   │   │   │   ├── ProductAdded.java
    │   │   │   │   ├── ProductDeleted.java
    │   │   │   │   └── ProductUpdated.java
    │   │   │   └── generic
    │   │   │       ├── AggregateRoot.java
    │   │   │       ├── ChangeEventSubscriber.java
    │   │   │       ├── Command.java
    │   │   │       ├── DomainEvent.java
    │   │   │       ├── DomainEventRepository.java
    │   │   │       ├── EventChange.java
    │   │   │       ├── EventStoreRepository.java
    │   │   │       └── StoredEvent.java
    │   │   ├── infrastructure
    │   │   │   ├── controllers
    │   │   │   │   ├── CommandController.java
    │   │   │   │   └── QueryController.java
    │   │   │   ├── generic
    │   │   │   │   ├── AbstractSerializer.java
    │   │   │   │   ├── CommandSerializer.java
    │   │   │   │   ├── DeserializeException.java
    │   │   │   │   ├── EventSerializer.java
    │   │   │   │   ├── StoredEventSerializer.java
    │   │   │   │   └── UseCaseHandler.java
    │   │   │   ├── handlers
    │   │   │   │   ├── AddProductUseCaseHandler.java
    │   │   │   │   ├── DeleteProductUseCaseHandler.java
    │   │   │   │   └── UpdateProductUseCaseHandler.java
    │   │   │   ├── materializers
    │   │   │   │   └── ProgramHandle.java
    │   │   │   ├── MessageService.java
    │   │   │   └── repositories
    │   │   │       └── MongoEventStoreRepository.java
    │   │   └── usecases
    │   │       ├── AddProductUseCase.java
    │   │       ├── DeleteProductUseCase.java
    │   │       └── UpdateProductUseCase.java
    │   └── resources
    │       ├── application.properties
    │       ├── static
    │       └── templates
    └── test
        └── java
            └── com
                └── example
                    └── hexagonaldemo
                        └── HexagonaldemoApplicationTests.java

