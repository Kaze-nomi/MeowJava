# Семинар 1

▎Что позволяет нам ООП

Объектно-ориентированное программирование (ООП) позволяет моделировать реальный мир с помощью объектов, упрощая разработку, поддержку и расширяемость кода.  
Пример: В приложении для магазина можно создать объекты "Товар", "Корзина" и "Покупатель".

---

▎Реализация

Реализация — это процесс создания конкретного функционала, описанного интерфейсами или абстрактными классами.  
Пример: Интерфейс Animal может иметь метод makeSound(), а класс Dog реализует его как bark().

---

▎Ассоциация

Ассоциация описывает связь между двумя объектами, например, один объект может ссылаться на другой.  
Пример: Объект "Учитель" связан с объектами "Студенты" через список студентов.

---

▎Композиция

Композиция — это "жёсткая" связь, при которой один объект не может существовать без другого.  
Пример: Объект "Человек" содержит объект "Сердце", и без сердца человек не существует.

---

▎Агрегация

Агрегация — это "слабая" связь, при которой объект может существовать отдельно от другого.  
Пример: Объект "Университет" агрегирует объекты "Студенты", но студенты могут существовать вне университета.

---

▎Полиморфизм

Полиморфизм позволяет одному интерфейсу иметь множество реализаций.  
Пример: Метод draw() может быть реализован по-разному для классов Circle и Square.

---

▎Наследование

Наследование позволяет одному классу унаследовать свойства и методы другого класса.  
Пример: Класс Car наследует свойства класса Vehicle, такие как скорость или тип двигателя.

---

▎Инкапсуляция

Инкапсуляция скрывает детали реализации объекта и предоставляет доступ только к необходимым данным через методы.  
Пример: Поле balance в классе BankAccount может быть приватным, а доступ к нему осуществляется через методы getBalance() и deposit().

---

▎Уникальный факт

Java поддерживает только одиночное наследование классов (один родительский класс), но позволяет множественное наследование через интерфейсы. Это помогает избежать проблем "алмаза" в наследовании.

# Семинар 2

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

▎Уникальный факт

Принципы KISS и Бритва Оккама активно используются не только в программировании, но и в инженерии и науке для упрощения сложных систем и моделей.

# Семинар 3

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

▎Уникальный факт

Mockito был создан для упрощения тестирования сложных зависимостей в Java-приложениях и стал одной из самых популярных библиотек для мокинга.

# Семинар 4

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

▎Уникальный факт

JaCoCo и Checkstyle можно интегрировать с CI/CD системами (например, GitHub Actions), чтобы автоматически проверять качество и покрытие кода при каждом коммите.

# Семинар 5

▎Singleton (Одиночка)

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

▎Factory (Фабрика)

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

▎Factory Method (Фабричный метод)

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

▎Abstract Factory (Абстрактная фабрика)

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

▎Builder (Строитель)

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

▎Prototype (Прототип)

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

▎Уникальный факт

Паттерн Singleton часто становится антипаттерном, если используется неправильно, так как нарушает принцип единственной ответственности (SRP) и может усложнять тестирование кода.

# Семинар 6

▎Цепочка обязанностей (Chain of Responsibility)  
   Паттерн, который позволяет передавать запрос последовательно по цепочке обработчиков, пока один из них не обработает его.  
   *Пример*: В системе технической поддержки запросы пользователя передаются от оператора к специалисту, пока не найдётся тот, кто может решить проблему.  

   ```java
   abstract class Handler {
       protected Handler next;
       public void setNext(Handler next) { this.next = next; }
       public abstract void handleRequest(String request);
   }
   ```
   
▎Команда (Command)  
   Паттерн, который инкапсулирует запрос в виде объекта, позволяя параметризовать объекты действиями.  
   *Пример*: Удалённое управление телевизором с кнопками "включить", "выключить".  

   ```java
   interface Command { void execute(); }
   class TurnOnCommand implements Command { public void execute() { System.out.println("TV is ON"); } }
   ```

▎Интерпретатор (Interpreter)  
   Паттерн, который определяет грамматику языка и интерпретирует выражения этого языка.  
   *Пример*: Калькулятор, который интерпретирует математические выражения.  

   ```java
   interface Expression { int interpret(); }
   class Number implements Expression { int value; public Number(int value) { this.value = value; } public int interpret() { return value; } }
   ```

▎Итератор (Iterator)  
   Паттерн, который предоставляет способ последовательного доступа к элементам коллекции без раскрытия её внутренней структуры.  
   *Пример*: Перебор списка пользователей в приложении.  

   ```java
   List<String> list = Arrays.asList("Alice", "Bob", "Charlie");
   Iterator<String> iterator = list.iterator();
   while(iterator.hasNext()) { System.out.println(iterator.next()); }
   ```

▎Посредник (Mediator)  
   Паттерн, который обеспечивает взаимодействие между объектами через центральный объект-посредник.  
   *Пример*: Чат-комната, где сообщения передаются через сервер.  

   ```java
   interface Mediator { void sendMessage(String message, User user); }
   ```

▎Хранитель (Memento)  
   Паттерн, который позволяет сохранять и восстанавливать состояние объекта без нарушения его инкапсуляции.  
   *Пример*: Функция отмены действий в текстовом редакторе.  

   ```java
   class Memento { private String state; public Memento(String state) { this.state = state; } public String getState() { return state; } }
   ```

▎Наблюдатель (Observer)  
   Паттерн, который создаёт механизм подписки для получения уведомлений об изменении состояния объекта.  
   *Пример*: Уведомления о новых сообщениях в социальных сетях.

   ```java
   interface Observer { void update(String message); }
   class User implements Observer { public void update(String message) { System.out.println("New notification: " + message); } }
   ```

▎Состояние (State)  
   Паттерн, который позволяет объекту изменять своё поведение в зависимости от своего состояния.  
   *Пример*: Состояние "игра" или "пауза" в приложении для игр.  

   ```java
   interface State { void handle(); }
   class PlayState implements State { public void handle() { System.out.println("Playing..."); } }
   ```

▎Стратегия (Strategy)  
   Паттерн, который определяет семейство алгоритмов и делает их взаимозаменяемыми.  
   *Пример*: Выбор метода сортировки в зависимости от размера массива.  

   ```java
   interface Strategy { void execute(); }
   class QuickSort implements Strategy { public void execute() { System.out.println("QuickSort applied"); } }
   ```

▎Шаблонный метод (Template Method)  
    Паттерн, который задаёт общий алгоритм выполнения задачи с возможностью переопределения отдельных шагов в подклассах.  
    *Пример*: Алгоритм приготовления кофе или чая (заварить воду, добавить ингредиенты).  

   ```java
    abstract class Beverage { final void prepare() { boilWater(); addIngredients(); } abstract void addIngredients(); void boilWater() { System.out.println("Boiling water");}}
   ```

▎Посетитель (Visitor)
    Паттерн, который позволяет добавлять новые операции к существующим объектам без изменения их структуры.  
    *Пример*: Подсчёт стоимости товаров в корзине интернет-магазина.  

   ```java
    interface Visitor { void visit(Book book); void visit(Fruit fruit); }
   ```

---

▎Уникальный факт

Паттерны проектирования были впервые систематизированы в книге "Design Patterns: Elements of Reusable Object-Oriented Software" (1994), написанной "Бандой четырёх". Эти принципы до сих пор остаются основой для разработки программного обеспечения и изучаются на всех уровнях обучения программированию.
    
# Семинар 7

▎Декоратор (Decorator)

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

▎Адаптер (Adapter)

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

▎Фасад (Facade)

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

▎Заместитель (Прокси) (Proxy)

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

▎Компоновщик (Composite)

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

▎Мост (Bridge)

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

▎Приспособленец (Flyweight)

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

▎Уникальный факт

Паттерн Фасад часто используется при проектировании библиотек и API, чтобы скрыть сложность внутренней реализации и предоставить разработчикам простой и интуитивно понятный интерфейс. Например, в Java javax.faces.context.FacesContext является примером фасада в Java EE.

# Семинар 8

▎DDD (Domain-Driven Design)  
   Это подход к разработке программного обеспечения, в котором акцент делается на бизнес-логику и модели предметной области. DDD помогает разделить систему на контексты (Bounded Contexts) и обеспечивает лучшее взаимодействие между разработчиками и бизнесом.  
   *Пример: В интернет-магазине можно разделить систему на контексты "Каталог товаров" и "Оформление заказа", чтобы каждая команда работала над своей частью.*

   ---

▎Event Storming  
   Это методика для совместного моделирования бизнес-процессов с помощью событий, которые происходят в системе. Она помогает выявить ключевые моменты, роли и взаимодействия в проекте.  
   *Пример: В ходе обсуждения процесса покупки участники отмечают события вроде "Пользователь добавил товар в корзину" или "Платеж подтвержден".*

   ---

▎JSON (JavaScript Object Notation)  
   Это текстовый формат данных, используемый для хранения и передачи структурированных данных, например, между клиентом и сервером. Он удобен из-за своей читаемости и легкости парсинга.  
   *Пример: {"name": "Иван", "age": 25} — JSON-объект, описывающий человека.*

   ---

▎Markdown  
   Это легковесный текстовый формат для разметки документов, который преобразуется в HTML или другие форматы. Используется для написания документации, заметок или README-файлов.  
   *Пример: *# Заголовок преобразуется в HTML в header.*

   ---

▎XML (Extensible Markup Language)  
   Это язык разметки для хранения и обмена данными, который позволяет задавать структуру с помощью тегов. XML часто используется в конфигурационных файлах или для передачи данных между системами.  
   *Пример: <user><name>Иван</name><age>25</age></user>.*

   ---

▎CSV (Comma-Separated Values)  
   Это текстовый формат для хранения табличных данных, где значения разделяются запятыми или другим разделителем. CSV прост в использовании и часто применяется для экспорта данных из таблиц или баз данных.  
   *Пример: name,age\nИван,25.*

   ---

▎Уникальный факт  

   Event Storming был придуман Альберто Брандолини, который утверждает, что "сложные проблемы лучше всего решаются с помощью простых инструментов".

# Семинар 9

▎CRUD (Create, Read, Update, Delete): это базовые операции для работы с данными в приложениях. Например, создание записи о пользователе (Create), получение списка пользователей (Read), обновление информации о пользователе (Update) и удаление пользователя (Delete).


▎@Controller vs @RestController:  

   • @Controller используется для обработки HTTP-запросов и возвращает представления (например, HTML).  

   • @RestController — это упрощённая версия, которая возвращает данные (например, JSON).  
   
   Пример: @RestController возвращает JSON-ответ в API, а @Controller — HTML-страницу.

---

▎@RequestMapping vs @GetMapping vs @PostMapping vs @PutMapping vs @DeleteMapping:  

   - @RequestMapping задаёт общий путь для всех HTTP-методов.  

   - Остальные аннотации уточняют конкретный HTTP-метод:  

     - @GetMapping — для получения данных.  

     - @PostMapping — для создания ресурсов.  

     - @PutMapping — для обновления.  

     - @DeleteMapping — для удаления.
   
   Пример: @GetMapping("/users") возвращает список пользователей.

   ---

▎@PathVariable vs @RequestBody vs @RequestParam:  

   - @PathVariable извлекает переменную из пути URL (например, /users/{id}).  

   - @RequestBody принимает данные из тела запроса (обычно JSON).  

   - @RequestParam извлекает параметры из строки запроса (например, ?name=John).  
   
   Пример: GET /users/1?role=admin — id берётся через @PathVariable, а role через @RequestParam.

   ---

▎@Valid + @Pattern + @Min + @Max + @Nullable + @NotNull:  
   Эти аннотации используются для валидации данных:  

   - @Valid запускает проверку объекта на соответствие правилам.  

   - @Pattern проверяет строку на соответствие регулярному выражению.  

   - @Min/@Max задают минимальные и максимальные значения чисел.  

   - @Nullable допускает значение null.  

   - @NotNull запрещает значение null.  
   
   Пример: поле возраста с аннотациями @NotNull @Min(18) требует, чтобы возраст был указан и был не менее 18.

   ---

▎Swagger + @Operation, OpenAPI:  
   Swagger — это инструмент для документирования и тестирования API. OpenAPI — это стандарт описания API, который поддерживает Swagger. Аннотация @Operation позволяет описывать методы API (например, их назначение). 
   
   Пример: Swagger генерирует интерфейс, где можно протестировать запросы к вашему API.

   ---

▎Уникальный факт 

В Spring можно комбинировать аннотации маршрутизации: например, использовать @RequestMapping на уровне класса для задания базового пути и @GetMapping на уровне метода для уточнения запроса.

# Семинар 10

▎Как экспортировать Swagger в Postman?

Swagger — это инструмент для документирования API, а Postman — это инструмент для тестирования API. Чтобы экспортировать спецификацию Swagger в Postman, нужно выполнить следующие шаги:

1. Откройте Swagger UI вашего API (обычно доступен по адресу /swagger-ui.html).

2. Найдите кнопку или ссылку для скачивания спецификации OpenAPI/Swagger в формате JSON или YAML (например, "Download JSON").

3. В Postman:

   • Нажмите "Import" (вверху слева).

   • Перетащите файл JSON/YAML или вставьте ссылку на спецификацию.

4. После импорта все эндпоинты из Swagger станут доступны в Postman для тестирования.

---

▎Что такое MockMvc и зачем он нужен?

MockMvc — это инструмент из Spring Framework для тестирования контроллеров MVC без необходимости запускать весь сервер приложения. Это позволяет быстро и изолированно проверять логику контроллеров.

Он нужен для:

• Тестирование контроллеров без запуска веб-сервера.

• Проверка HTTP-запросов и ответов.

• Ускорение процесса тестирования.

---

▎Уникальный факт

MockMvc поддерживает тестирование фильтров безопасности Spring Security. Вы можете добавлять авторизационные токены или настраивать роли пользователей прямо в тестах. 

Например:

```java
mockMvc.perform(get("/admin")
        .with(user("admin").roles("ADMIN")))
       .andExpect(status().isOk());
```

# Семинар 11

▎Что такое Docker? Зачем он нужен?

Docker — это платформа для контейнеризации приложений. Он позволяет упаковать приложение и его зависимости в контейнер, который можно запускать на любом сервере, где установлен Docker. Это упрощает развертывание, тестирование и переносимость приложений.

Пример из жизни: Представь, что у тебя есть приложение, которое требует определённую версию Java и PostgreSQL. С Docker ты можешь создать контейнеры с этими зависимостями и не беспокоиться о том, что на сервере может быть другая версия ПО.

```shell
docker run hello-world
```

---

▎Как поднять БД в Docker?

Для поднятия базы данных в Docker используется команда docker run. Например, для PostgreSQL:

```shell
docker run --name my-postgres -e POSTGRES_PASSWORD=mysecretpassword -d postgres
```

Здесь мы создаём контейнер с PostgreSQL, задаём пароль для пользователя postgres и запускаем его в фоновом режиме (-d). После этого база данных доступна на порту 5432.

---

▎Как подключить БД к приложению?

Для подключения приложения к БД нужно указать параметры подключения (хост, порт, имя пользователя, пароль). Например, в Java с использованием Hibernate или JDBC:

```java
Properties props = new Properties();
props.setProperty("hibernate.connection.url", "jdbc:postgresql://localhost:5432/mydb");
props.setProperty("hibernate.connection.username", "postgres");
props.setProperty("hibernate.connection.password", "mysecretpassword");
```

В файле application.properties для Spring Boot это будет выглядеть так:

```java
spring.datasource.url=jdbc:postgresql://localhost:5432/mydb
spring.datasource.username=postgres
spring.datasource.password=mysecretpassword
```

---

▎Что такое Repository?

Repository — это паттерн проектирования, который используется для работы с базой данных. В Java, например, в Spring Data JPA репозиторий представляет собой интерфейс, который предоставляет методы для операций CRUD.

Пример:

```java
@Repository
public interface UserRepository extends JpaRepository<User, Long> {
    Optional<User> findByUsername(String username);
}
```

Этот интерфейс автоматически предоставляет методы для работы с сущностью User.

---

▎Что такое Hibernate?

Hibernate — это ORM-фреймворк (Object-Relational Mapping), который позволяет работать с базой данных через объекты Java. Он автоматически преобразует объекты в записи таблиц и наоборот.

Пример:

```java
@Entity
public class User {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;
    private String username;
    private String password;
}
```

В этом примере класс User мапится на таблицу в базе данных.

---

▎Связь one-to-one, one-to-many, many-to-many в Java

• One-to-One (один-к-одному): Один объект связан с одним другим объектом.

```java
@Entity
public class User {
    @OneToOne
    private Profile profile;
}
```

• One-to-Many (один-ко-многим): Один объект связан с несколькими другими объектами.

```java
@Entity
public class User {
    @OneToMany(mappedBy = "user")
    private List<Post> posts;
}
```

• Many-to-Many (многие-ко-многим): Несколько объектов связаны с несколькими другими объектами.

```java
@Entity
public class Student {
    @ManyToMany
    private List<Course> courses;
}
```

---

▎Как сделать общую таблицу для разных объектов?

В Hibernate можно использовать стратегию наследования @Inheritance. Например:

```java
@Entity
@Inheritance(strategy = InheritanceType.SINGLE_TABLE)
public abstract class Vehicle {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;
    private String name;
}

@Entity
public class Car extends Vehicle {
    private int numberOfDoors;
}

@Entity
public class Bike extends Vehicle {
    private boolean hasPedals;
}
```

Здесь Car и Bike будут храниться в одной таблице Vehicle.

---

▎Уникальный факт

Docker позволяет запускать несколько экземпляров одной и той же базы данных с разными конфигурациями на одном сервере. Это удобно для тестирования разных окружений. Например, можно запустить PostgreSQL версии 12 и версии 15 параллельно без конфликтов.

# Семинар 12

▎Как в проекте происходит версионирование? Как его подключить?  

Версионирование в проекте обычно осуществляется с использованием систем контроля версий, таких как Git. Это позволяет отслеживать изменения в коде, возвращаться к предыдущим версиям и работать в команде над одним проектом.  

Пример:

```git
git init
git add .
git commit -m "Initial commit"
```

Для подключения к удаленному репозиторию используется команда git remote add origin <url>.

---

▎Как в системе версионирования создать таблицу? Как создать внешний ключ?  

Для управления версиями базы данных часто используют инструменты миграции, такие как Flyway или Liquibase. В Flyway создаются SQL-скрипты для создания таблиц и внешних ключей. 

Пример SQL-скрипта:

```sql
CREATE TABLE users (
    id SERIAL PRIMARY KEY,
    name VARCHAR(100)
);

CREATE TABLE orders (
    id SERIAL PRIMARY KEY,
    user_id INT,
    FOREIGN KEY (user_id) REFERENCES users(id)
);
```

---

▎Как поднять приложение в Docker?  
Для запуска приложения в Docker необходимо создать Dockerfile и описать в нем инструкции для сборки контейнера. Затем с помощью команды docker build создается образ, а docker run запускает контейнер.  

Пример Dockerfile для Java-приложения:

```dockerfile
FROM openjdk:17
COPY target/app.jar app.jar
ENTRYPOINT ["java", "-jar", "app.jar"]

Команды для сборки и запуска:  
docker build -t my-app .
docker run -p 8080:8080 my-app
```

---

▎Что значит параметр ddl-auto? Какие у него есть параметры?  

Параметр spring.jpa.hibernate.ddl-auto используется для управления стратегией создания и обновления схемы базы данных в Hibernate. Он может принимать значения:  

• create — создать схему при запуске приложения;  

• update — обновить схему без удаления данных;  

• validate — проверить соответствие схемы базы данных модели;  

• none — не выполнять никаких действий.  

Пример:

spring.jpa.hibernate.ddl-auto=update

---

▎Как сделать связь один ко многим?  

Связь "один ко многим" можно реализовать с помощью аннотаций Hibernate/JPA. Например, одна сущность "User" может иметь много "Order".

Пример:

```java
@Entity
public class User {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    @OneToMany(mappedBy = "user", cascade = CascadeType.ALL)
    private List<Order> orders;
}

@Entity
public class Order {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    @ManyToOne
    @JoinColumn(name = "user_id")
    private User user;
}
```

---

▎Уникальный факт

Flyway поддерживает версионирование не только SQL-скриптов, но и Java-классов для миграций, что позволяет писать сложную логику миграции на Java вместо SQL.
