# Семинар 1:

▎Что позволяет нам ООП:

Объектно-ориентированное программирование (ООП) позволяет моделировать реальный мир с помощью объектов, упрощая разработку, поддержку и расширяемость кода.  
Пример: В приложении для магазина можно создать объекты "Товар", "Корзина" и "Покупатель".

---

▎Реализация:

Реализация — это процесс создания конкретного функционала, описанного интерфейсами или абстрактными классами.  
Пример: Интерфейс Animal может иметь метод makeSound(), а класс Dog реализует его как bark().

---

▎Ассоциация:

Ассоциация описывает связь между двумя объектами, например, один объект может ссылаться на другой.  
Пример: Объект "Учитель" связан с объектами "Студенты" через список студентов.

---

▎Композиция:

Композиция — это "жёсткая" связь, при которой один объект не может существовать без другого.  
Пример: Объект "Человек" содержит объект "Сердце", и без сердца человек не существует.

---

▎Агрегация:

Агрегация — это "слабая" связь, при которой объект может существовать отдельно от другого.  
Пример: Объект "Университет" агрегирует объекты "Студенты", но студенты могут существовать вне университета.

---

▎Полиморфизм:

Полиморфизм позволяет одному интерфейсу иметь множество реализаций.  
Пример: Метод draw() может быть реализован по-разному для классов Circle и Square.

---

▎Наследование:

Наследование позволяет одному классу унаследовать свойства и методы другого класса.  
Пример: Класс Car наследует свойства класса Vehicle, такие как скорость или тип двигателя.

---

▎Инкапсуляция:

Инкапсуляция скрывает детали реализации объекта и предоставляет доступ только к необходимым данным через методы.  
Пример: Поле balance в классе BankAccount может быть приватным, а доступ к нему осуществляется через методы getBalance() и deposit().

---

▎Уникальный факт:

Java поддерживает только одиночное наследование классов (один родительский класс), но позволяет множественное наследование через интерфейсы. Это помогает избежать проблем "алмаза" в наследовании.





# Семинар 2:

▎KISS (Keep It Simple, Stupid)

Принцип гласит: "Делай проще". Сложные решения увеличивают вероятность ошибок.  
Пример: Вместо создания сложного алгоритма для сортировки списка, можно использовать встроенные методы языка программирования, такие как list.sort() в Python.

---

▎DRY (Don't Repeat Yourself)

Не дублируйте код. Если часть кода повторяется, вынесите её в функцию или модуль.  
Пример: Вместо копирования одного и того же SQL-запроса в разных местах, можно создать отдельную функцию get_user_by_id(id).

---

▎YAGNI (You Aren't Gonna Need It)

Не добавляйте функционал, который может никогда не понадобиться.  
Пример: Не стоит писать код для обработки 1000+ пользователей, если приложение рассчитано на максимум 10.

---

▎BDUF (Big Design Up Front)

Это подход к разработке, где вся система проектируется заранее.  
Пример: Перед началом проекта пишется детальная документация о том, как будут работать все модули системы.

---

▎SOLID

1. S - *Single Responsibility Principle*: У каждого класса должна быть одна ответственность.  
   Пример: Класс User отвечает только за хранение данных пользователя, а не за их валидацию.  

2. O - *Open/Closed Principle*: Код должен быть открыт для расширения, но закрыт для изменений.  
   Пример: Добавление нового типа оплаты через интерфейсы, без изменения существующего кода.  

3. L - *Liskov Substitution Principle*: Объекты подкласса должны заменять объекты родительского класса без ошибок.  
   Пример: Если Bird имеет метод fly(), то подкласс Penguin не должен нарушать это поведение.  

4. I - *Interface Segregation Principle*: Интерфейсы должны быть узкоспециализированными.  
   Пример: Лучше несколько интерфейсов (IPrinter, IScanner), чем один огромный (IMultifunctionDevice).  

5. D - *Dependency Inversion Principle*: Модули высокого уровня не должны зависеть от низкоуровневых модулей напрямую. Используйте абстракции.  
   Пример: Вместо использования конкретного класса базы данных, работайте через интерфейс Database.

---

▎APO (Automatic Programming Optimization)

Это подход, при котором оптимизация кода или его генерация выполняется автоматически с использованием инструментов или компиляторов.  
Пример: Современные компиляторы могут автоматически оптимизировать цикл, чтобы сократить время выполнения.

---

▎Бритва Оккама

Принцип, который гласит: "Не усложняй без необходимости". Если есть два решения, выбирайте более простое.  
Пример: Для хранения настроек приложения лучше использовать JSON-файл вместо сложной базы данных, если это оправдано.

---

▎Stream API

Инструмент для работы с потоками данных в Java. Позволяет фильтровать, преобразовывать и обрабатывать коллекции данных.  
Основные методы: filter(), map(), reduce(), collect().  
Пример: С помощью stream().filter(x -> x > 10) можно отфильтровать элементы больше 10.

---

▎Уникальный факт:

Принципы KISS и Бритва Оккама активно используются не только в программировании, но и в инженерии и науке для упрощения сложных систем и моделей.

---

# Семинар 3:

▎Service Locator

Шаблон проектирования, предоставляющий центральный объект для поиска нужных сервисов. Например, в приложении можно использовать ServiceLocator для поиска базы данных или логгера без прямой зависимости от их реализации.  
```java
Logger logger = ServiceLocator.getService(Logger.class);
logger.log("Пример использования ServiceLocator");
```

---

▎DIP (Dependency Inversion Principle)

Принцип SOLID, согласно которому модули верхнего уровня не должны зависеть от модулей нижнего уровня, а оба должны зависеть от абстракций. Например, вместо зависимости от конкретного класса репозитория, код использует интерфейс.  

```java
interface Repository {
    void save(String data);
}
```

---

▎IoC (Inversion of Control)

Принцип, при котором управление зависимостями передается внешнему контейнеру, а не реализуется вручную в коде. В Spring IoC контейнер автоматически внедряет зависимости через аннотации.  

```java
@Autowired
private Service service;
```

---

▎Singleton

Шаблон проектирования, который гарантирует, что класс имеет только один экземпляр и предоставляет глобальную точку доступа к нему. Например, класс для логирования в приложении может быть реализован как Singleton.  

```java
public class Logger {
    private static Logger instance = new Logger();
    private Logger() {}
    public static Logger getInstance() {
        return instance;
    }
}
```

---

▎Prototype

Шаблон проектирования, позволяющий создавать новые объекты путем клонирования существующих. Например, если у вас есть объект с большим количеством настроек, вы можете клонировать его вместо создания заново.  

```java
Car prototypeCar = new Car("Red", "Sedan");
Car clonedCar = prototypeCar.clone();
```

---

▎Юнит тесты JUnit

Тесты, проверяющие работу отдельных модулей или методов приложения. Например, с помощью JUnit можно протестировать метод сложения чисел.  

```java
@Test
public void testAddition() {
    assertEquals(5, Calculator.add(2, 3));
}
```

---

▎Mockito (mock + spy)

Mockito позволяет создавать mock-объекты (имитации) для тестирования зависимостей. Spy используется для частичного контроля над реальными объектами.  

```java
MyService mockService = Mockito.mock(MyService.class);
Mockito.when(mockService.getData()).thenReturn("Mocked Data");
```

---

▎@SpringBootTest

Аннотация Spring Boot для интеграционного тестирования всего приложения. Она поднимает контекст Spring и позволяет тестировать все уровни приложения.  

```java
@SpringBootTest
public class ApplicationTests {
    @Test
    void contextLoads() {}
}
```

---

▎@Autowired

Аннотация для автоматического внедрения зависимостей в классы Spring. Например, вы можете внедрить сервис в контроллер без явного создания объекта.  

```java
@Autowired
private MyService myService;
```

---

▎@Component

Аннотация для обозначения класса как компонента Spring, чтобы его можно было автоматически обнаружить и зарегистрировать в контексте. Например, если класс помечен как @Component, его экземпляр будет создан автоматически.  

```java
@Component
public class MyComponent {
    public void doWork() {
        System.out.println("Работа выполнена");
    }
}
```

---

▎Уникальный факт:

Mockito был создан для упрощения тестирования сложных зависимостей в Java-приложениях и стал одной из самых популярных библиотек для мокинга.

---

# Семинар 4:

▎@Bean

Определение:  
@Bean используется для создания объекта (бина), который будет управляться Spring. Аннотация применяется к методу, возвращающему бин.  

Пример из жизни:  
Вы заказываете пиццу в ресторане, и вам приносят готовое блюдо — это бин, созданный по рецепту.  

Пример кода:
```java
@Bean
public Pizza pizza() {
    return new Pizza("Pepperoni");
}
```

---

▎@Configuration

Определение:  
@Configuration указывает, что класс содержит определения бинов и их зависимости. Это своего рода "рецепт" для создания объектов в Spring.  

Пример из жизни:  
Книга рецептов, где каждый рецепт описывает, как приготовить блюдо (бин).  

Пример кода:
```java
@Configuration
public class AppConfig {
    @Bean
    public Pizza pizza() {
        return new Pizza("Margherita");
    }
}
```

---

▎Jacoco

Определение:  
JaCoCo — это инструмент для проверки покрытия кода тестами, показывающий, сколько строк кода было выполнено во время тестирования.  

Как включить:  
Добавить плагин в Maven или Gradle.

---

▎Checkstyle

Определение:  
Checkstyle — это инструмент для проверки стиля и качества кода на соответствие заданным правилам.  

Как включить:
Добавить плагин в Maven или Gradle.

---

▎application.yml

Определение:  
application.yml — это файл конфигурации Spring Boot, в котором задаются параметры приложения (например, порт сервера или настройки базы данных).  

Пример:
```yml
server:
  port: 8080

spring:
  datasource:
    url: jdbc:mysql://localhost:3306/mydb
    username: user
    password: pass
```

---

▎Уникальный факт:

JaCoCo и Checkstyle можно интегрировать с CI/CD системами (например, GitHub Actions), чтобы автоматически проверять качество и покрытие кода при каждом коммите.

---

# Семинар 5:

▎1. Singleton (Одиночка)

Определение: Порождающий паттерн, который гарантирует, что у класса есть только один экземпляр, и предоставляет глобальную точку доступа к нему.  
Пример из жизни: В приложении может быть только один объект логгера, чтобы все модули писали логи в одно место.  
Реализация в Java:
```java
public class Singleton {
    private static Singleton instance;

    private Singleton() {}

    public static Singleton getInstance() {
        if (instance == null) {
            instance = new Singleton();
        }
        return instance;
    }
}
```

---

▎2. Factory (Фабрика)

Определение: Порождающий паттерн, который создает объекты без указания конкретных классов.  
Пример из жизни: Вы заказываете еду в ресторане, а кухня решает, как приготовить блюдо.  
Реализация в Java:
```java
public class ShapeFactory {
    public Shape getShape(String shapeType) {
        if (shapeType.equalsIgnoreCase("CIRCLE")) {
            return new Circle();
        } else if (shapeType.equalsIgnoreCase("RECTANGLE")) {
            return new Rectangle();
        }
        return null;
    }
}
```

---

▎3. Factory Method (Фабричный метод)

Определение: Порождающий паттерн, который определяет интерфейс для создания объектов, но позволяет подклассам изменять тип создаваемых объектов.  
Пример из жизни: В кофейне разные бариста (подклассы) могут готовить разные виды кофе.  
Реализация в Java:
```java
abstract class ShapeCreator {
    public abstract Shape createShape();
}

class CircleCreator extends ShapeCreator {
    public Shape createShape() {
        return new Circle();
    }
}

class RectangleCreator extends ShapeCreator {
    public Shape createShape() {
        return new Rectangle();
    }
}
```

---

▎4. Abstract Factory (Абстрактная фабрика)

Определение: Порождающий паттерн, который предоставляет интерфейс для создания семейств связанных объектов без указания их конкретных классов.  
Пример из жизни: Фабрика мебели может производить семейства объектов, например, "Викторианская мебель" или "Современная мебель".  
Реализация в Java:
```java
interface FurnitureFactory {
    Chair createChair();
    Table createTable();
}

class VictorianFurnitureFactory implements FurnitureFactory {
    public Chair createChair() { return new VictorianChair(); }
    public Table createTable() { return new VictorianTable(); }
}
```


---

▎5. Builder (Строитель)

Определение: Порождающий паттерн, который позволяет пошагово создавать сложные объекты.  
Пример из жизни: Строительство дома: сначала строится фундамент, затем стены, крыша и т.д.  
Реализация в Java:

```java
public class House {
    private String foundation;
    private String walls;
    private String roof;

    public static class Builder {
        private String foundation;
        private String walls;
        private String roof;

        public Builder setFoundation(String foundation) {
            this.foundation = foundation;
            return this;
        }

        public Builder setWalls(String walls) {
            this.walls = walls;
            return this;
        }

        public Builder setRoof(String roof) {
            this.roof = roof;
            return this;
        }

        public House build() {
            House house = new House();
            house.foundation = this.foundation;
            house.walls = this.walls;
            house.roof = this.roof;
            return house;
        }
    }
}
```

---

▎6. Prototype (Прототип)

Определение: Порождающий паттерн, который позволяет копировать объекты без зависимости от их конкретных классов.  
Пример из жизни: Клонирование документов в офисе.  
Реализация в Java:
```java
public class Prototype implements Cloneable {
    private String field;

    public Prototype(String field) {
        this.field = field;
    }

    @Override
    protected Object clone() throws CloneNotSupportedException {
        return super.clone();
    }
}
```

---

▎Уникальный факт:

Паттерн Singleton часто становится антипаттерном, если используется неправильно, так как нарушает принцип единственной ответственности (SRP) и может усложнять тестирование кода.

---

# Семинар 6:

▎Поведенческие паттерны

1. Цепочка обязанностей (Chain of Responsibility)  
   Паттерн, который позволяет передавать запрос последовательно по цепочке обработчиков, пока один из них не обработает его.  
   *Пример*: В системе технической поддержки запросы пользователя передаются от оператора к специалисту, пока не найдётся тот, кто может решить проблему.  

   ```java
   abstract class Handler {
       protected Handler next;
       public void setNext(Handler next) { this.next = next; }
       public abstract void handleRequest(String request);
   }
   ```
   
1. Команда (Command)  
   Паттерн, который инкапсулирует запрос в виде объекта, позволяя параметризовать объекты действиями.  
   *Пример*: Удалённое управление телевизором с кнопками "включить", "выключить".  

   ```java
   interface Command { void execute(); }
   class TurnOnCommand implements Command { public void execute() { System.out.println("TV is ON"); } }
   ```

2. Интерпретатор (Interpreter)  
   Паттерн, который определяет грамматику языка и интерпретирует выражения этого языка.  
   *Пример*: Калькулятор, который интерпретирует математические выражения.  

   ```java
   interface Expression { int interpret(); }
   class Number implements Expression { int value; public Number(int value) { this.value = value; } public int interpret() { return value; } }
   ```

3. Итератор (Iterator)  
   Паттерн, который предоставляет способ последовательного доступа к элементам коллекции без раскрытия её внутренней структуры.  
   *Пример*: Перебор списка пользователей в приложении.  

   ```
   List<String> list = Arrays.asList("Alice", "Bob", "Charlie");
   Iterator<String> iterator = list.iterator();
   while(iterator.hasNext()) { System.out.println(iterator.next()); }
   ```

4. Посредник (Mediator)  
   Паттерн, который обеспечивает взаимодействие между объектами через центральный объект-посредник.  
   *Пример*: Чат-комната, где сообщения передаются через сервер.  

   ```java
   interface Mediator { void sendMessage(String message, User user); }
   ```

6. Хранитель (Memento)  
   Паттерн, который позволяет сохранять и восстанавливать состояние объекта без нарушения его инкапсуляции.  
   *Пример*: Функция отмены действий в текстовом редакторе.  

   ```java
   class Memento { private String state; public Memento(String state) { this.state = state; } public String getState() { return state; } }
   ```

8. Наблюдатель (Observer)  
   Паттерн, который создаёт механизм подписки для получения уведомлений об изменении состояния объекта.  
   *Пример*: Уведомления о новых сообщениях в социальных сетях.

   ```java
   interface Observer { void update(String message); }
   class User implements Observer { public void update(String message) { System.out.println("New notification: " + message); } }
   ```

8. Состояние (State)  
   Паттерн, который позволяет объекту изменять своё поведение в зависимости от своего состояния.  
   *Пример*: Состояние "игра" или "пауза" в приложении для игр.  

   ```java
   interface State { void handle(); }
   class PlayState implements State { public void handle() { System.out.println("Playing..."); } }
   ```

9. Стратегия (Strategy)  
   Паттерн, который определяет семейство алгоритмов и делает их взаимозаменяемыми.  
   *Пример*: Выбор метода сортировки в зависимости от размера массива.  

   ```java
   interface Strategy { void execute(); }
   class QuickSort implements Strategy { public void execute() { System.out.println("QuickSort applied"); } }
   ```

10. Шаблонный метод (Template Method)  
    Паттерн, который задаёт общий алгоритм выполнения задачи с возможностью переопределения отдельных шагов в подклассах.  
    *Пример*: Алгоритм приготовления кофе или чая (заварить воду, добавить ингредиенты).  

    ```java
    abstract class Beverage { final void prepare() { boilWater(); addIngredients(); } abstract void addIngredients(); void boilWater() { System.out.println("Boiling water"); } }
    ```

11. Посетитель (Visitor)
    Паттерн, который позволяет добавлять новые операции к существующим объектам без изменения их структуры.  
    *Пример*: Подсчёт стоимости товаров в корзине интернет-магазина.  

    ```java
    interface Visitor { void visit(Book book); void visit(Fruit fruit); }
    ```

---

▎Уникальный факт:

Паттерны проектирования были впервые систематизированы в книге "Design Patterns: Elements of Reusable Object-Oriented Software" (1994), написанной "Бандой четырёх". Эти принципы до сих пор остаются основой для разработки программного обеспечения и изучаются на всех уровнях обучения программированию.

---

# Семинар 7:

▎1. Декоратор (Decorator)

Определение: Паттерн, позволяющий динамически добавлять объектам новую функциональность, не изменяя их код.  
Пример из жизни: Обёртывание подарка в несколько слоёв упаковки (каждый слой добавляет что-то новое).  
Пример кода:

```java
interface Coffee {
    String getDescription();
    double getCost();
}

class SimpleCoffee implements Coffee {
    public String getDescription() { return "Simple coffee"; }
    public double getCost() { return 5; }
}

class MilkDecorator implements Coffee {
    private Coffee coffee;
    public MilkDecorator(Coffee coffee) { this.coffee = coffee; }
    public String getDescription() { return coffee.getDescription() + ", milk"; }
    public double getCost() { return coffee.getCost() + 2; }
}
```

---

▎2. Адаптер (Adapter)

Определение: Паттерн, который позволяет объекту с одним интерфейсом работать с другим несовместимым интерфейсом.  
Пример из жизни: Зарядное устройство для телефона, которое преобразует высокое напряжение в подходящее.  
Пример кода:

```java
interface USB {
    void connectWithUsbCable();
}

class TypeCPhone {
    void connectWithTypeC() { System.out.println("Connected with Type-C"); }
}

class UsbToTypeCAdapter implements USB {
    private TypeCPhone phone;
    UsbToTypeCAdapter(TypeCPhone phone) { this.phone = phone; }
    public void connectWithUsbCable() { phone.connectWithTypeC(); }
}
```

---

▎3. Фасад (Facade)

Определение: Паттерн, предоставляющий простой интерфейс для работы с сложной системой.  
Пример из жизни: Универсальный пульт управления телевизором, звуком и кондиционером.  
Пример кода:

```java
class HomeTheaterFacade {
    private TV tv;
    private SoundSystem soundSystem;

    public HomeTheaterFacade(TV tv, SoundSystem soundSystem) {
        this.tv = tv;
        this.soundSystem = soundSystem;
    }

    public void watchMovie() {
        tv.turnOn();
        soundSystem.setVolume(10);
        System.out.println("Enjoy your movie!");
    }
}
```

---

▎4. Заместитель (Прокси) (Proxy)

Определение: Паттерн, который предоставляет объект-заместитель для контроля доступа к другому объекту.  
Пример из жизни: Секретарь, который фильтрует входящие звонки для директора.  
Пример кода:

```java
interface Image {
    void display();
}

class RealImage implements Image {
    private String filename;
    public RealImage(String filename) { this.filename = filename; loadFromDisk(); }
    private void loadFromDisk() { System.out.println("Loading " + filename); }
    public void display() { System.out.println("Displaying " + filename); }
}

class ProxyImage implements Image {
    private RealImage realImage;
    private String filename;

    public ProxyImage(String filename) { this.filename = filename; }
    public void display() {
        if (realImage == null) realImage = new RealImage(filename);
        realImage.display();
    }
}
```

---

▎5. Компоновщик (Composite)

Определение: Паттерн, позволяющий объединять объекты в древовидную структуру для удобной работы с ними как с единым целым.  
Пример из жизни: Папка на компьютере, которая может содержать как файлы, так и другие папки.  
Пример кода:

```java
interface FileSystemComponent {
    void showDetails();
}

class File implements FileSystemComponent {
    private String name;
    public File(String name) { this.name = name; }
    public void showDetails() { System.out.println("File: " + name); }
}

class Folder implements FileSystemComponent {
    private List<FileSystemComponent> components = new ArrayList<>();
    public void add(FileSystemComponent component) { components.add(component); }
    public void showDetails() { components.forEach(FileSystemComponent::showDetails); }
}
```

---

▎6. Мост (Bridge)

Определение: Паттерн, разделяющий абстракцию и реализацию, позволяя изменять их независимо друг от друга.  
Пример из жизни: Разделение пульта управления и конкретного устройства (телевизора или кондиционера).  
Пример кода:

```java
interface Device {
    void turnOn();
}

class TV implements Device {
    public void turnOn() { System.out.println("TV is ON"); }
}

class RemoteControl {
    protected Device device;
    public RemoteControl(Device device) { this.device = device; }
    public void pressPowerButton() { device.turnOn(); }
}
```

---

▎7. Приспособленец (Flyweight)

Определение: Паттерн, позволяющий экономить память за счёт разделения общего состояния между множеством объектов.  
Пример из жизни: Использование одного экземпляра шрифта для всех символов текста в документе.  
Пример кода:

```java
class TreeType {
    private String name;
    private String color;

    public TreeType(String name, String color) {
        this.name = name;
        this.color = color;
    }

    public void draw(int x, int y) {
        System.out.println("Drawing " + name + " at (" + x + ", " + y + ")");
    }
}

class TreeFactory {
    private static Map<String, TreeType> treeTypes = new HashMap<>();

    public static TreeType getTreeType(String name, String color) {
        treeTypes.putIfAbsent(name, new TreeType(name, color));
        return treeTypes.get(name);
    }
}
```

---

▎Уникальный факт:

Паттерн Фасад часто используется при проектировании библиотек и API, чтобы скрыть сложность внутренней реализации и предоставить разработчикам простой и интуитивно понятный интерфейс. Например, в Java javax.faces.context.FacesContext является примером фасада в Java EE.
