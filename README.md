# Тема 8. Введение в ООП
Отчет по Теме #8 выполнил(а):
- Легков Иван Сергеевич
- ПИЭ-21-1

| Задание | Лаб_раб | Сам_раб |
| ------ | ------ | ------ |
| Задание 1 | + | + |
| Задание 2 | + | + |
| Задание 3 | + | + |
| Задание 4 | + | + |
| Задание 5 | + | + |
| Задание 6 |  | |
| Задание 7 |  | |
| Задание 8 |  |  |
| Задание 9 |  |  |
| Задание 10 |  |  |

# Лабараторные работы 
   ## Лабараторная работа 1


  ```python
class Car:
    def __init__(self,make,model):
        self.make=make
        self.model=model

my_car = Car("Toyota","Corolla")
```
  ### Результат
  ![1](https://github.com/armuane/laba8/blob/main/Desktop/laba8/1.png?raw=true)

 
## Краткий вывод:
тот код создает класс Car с конструктором __init__, который принимает два аргумента: make (марка) и model (модель). Внутри конструктора эти значения присваиваются атрибутам self.make и self.model объекта класса.

Затем создается экземпляр класса my_car с аргументами "Toyota" и "Corolla". Таким образом, my_car становится объектом типа Car с маркой "Toyota" и моделью "Corolla".


   ## Лабараторная работа 2


  ```python
class Car:
    def __init__(self,make,model):
        self.make=make
        self.model=model
    def drive(self):
        print(f"Driving the {self.make} {self.model}")

my_car = Car("Toyota","Corolla")
my_car.drive()
```
  ### Результат
  ![2](https://github.com/armuane/laba8/blob/main/Desktop/laba8/2.png?raw=true)

 
## Краткий вывод:
Этот код также создает класс Car с конструктором __init__, который принимает два аргумента: make (марка) и model (модель). Внутри конструктора эти значения присваиваются атрибутам self.make и self.model объекта класса.

Однако в этом случае класс также имеет метод drive. Метод drive выводит сообщение о том, что происходит при вождении данного автомобиля, используя значения марки и модели, сохраненные в атрибутах.

Затем создается экземпляр класса my_car с аргументами "Toyota" и "Corolla". После этого вызывается метод drive() для объекта my_car, что приводит к выводу сообщения "Driving the Toyota Corolla".


   ## Лабараторная работа 3


  ```python
# Определение класса Car
class Car:
    def __init__(self, make, model):
        # Инициализация атрибутов make и model
        self.make = make
        self.model = model

    def drive(self):
        # Вывод сообщения о вождении с использованием марки и модели
        print(f"Driving the {self.make} {self.model}")

# Создание объекта my_car класса Car с маркой "Toyota" и моделью "Corolla"
my_car = Car("Toyota", "Corolla")
# Вызов метода drive для объекта my_car
my_car.drive()

# Определение подкласса ElectricCar, наследующего от класса Car
class ElectricCar(Car):
    def __init__(self, make, model, battery_capacity):
        # Вызов конструктора родительского класса с помощью super()
        super().__init__(make, model)
        # Инициализация атрибута battery_capacity для подкласса ElectricCar
        self.battery_capacity = battery_capacity

    def charge(self):
        # Вывод сообщения о зарядке с использованием марки, модели и емкости батареи
        print(f"Charging the {self.make} {self.model} with {self.battery_capacity} kWh")

# Создание объекта my_electric_car класса ElectricCar с маркой "Tesla", моделью "Model S" и емкостью батареи 75
my_electric_car = ElectricCar("Tesla", "Model S", 75)
# Вызов метода drive для объекта my_electric_car
my_electric_car.drive()
# Вызов метода charge для объекта my_electric_car
my_electric_car.charge()

```
  ### Результат
  ![3](https://github.com/armuane/laba8/blob/main/Desktop/laba8/3.png?raw=true)

 
## Краткий вывод:
В этом коде определен класс Car с методами __init__ и drive. Затем создается объект my_car класса Car с маркой "Toyota" и моделью "Corolla", и вызывается метод drive, что приводит к выводу "Driving the Toyota Corolla".

Затем определен подкласс ElectricCar, который наследует от класса Car. В конструкторе __init__ этого подкласса вызывается конструктор родительского класса с помощью super().__init__(make, model), чтобы унаследовать атрибуты make и model. Затем у подкласса ElectricCar добавляется новый атрибут battery_capacity.

Создается объект my_electric_car класса ElectricCar с маркой "Tesla", моделью "Model S" и емкостью батареи 75. Затем вызываются методы drive() и charge()


   ## Лабараторная работа 4


  ```python
# Определение класса Car
class Car:
    def __init__(self, make, model):
        # Инициализация атрибута _make с использованием единого подчеркивания (неявно указывает на "protected")
        self._make = make
        # Инициализация атрибута __model с использованием двух подчеркиваний (имеет защищенный доступ)
        self.__model = model

    def drive(self):
        # Вывод сообщения о вождении с использованием марки и модели
        print(f"Driving the {self._make} {self.__model}")

# Создание объекта my_car класса Car с маркой "Toyota" и моделью "Corolla"
my_car = Car("Toyota", "Corolla")

# Вывод значения атрибута _make (в общем случае, неявно считается защищенным)
print(my_car._make)

# Вызов метода drive для объекта my_car
my_car.drive()

```
  ### Результат
  ![4](https://github.com/armuane/laba8/blob/main/Desktop/laba8/4.png?raw=true)

 
## Краткий вывод:
Этот код определяет класс Car с атрибутами _make и __model. Использование одного подчеркивания перед именем атрибута (_make) обычно сигнализирует о том, что атрибут является "protected" (защищенным), что подразумевает, что его лучше не использовать вне класса, но это не является строгим правилом.

Использование двух подчеркиваний перед именем атрибута (__model) делает его "private" (приватным), что означает, что он не должен напрямую использоваться за пределами класса. Однако, в Python его все равно можно получить, но с другим именем (например, _Car__model). Но так делать не рекомендуется из-за нарушения инкапсуляции.

Затем создается объект my_car класса Car с маркой "Toyota" и моделью "Corolla". Выводится значение атрибута _make, и вызывается метод drive(), демонстрируя использование атрибутов и методов класса.


   ## Лабараторная работа 5


  ```python
# Определение базового класса Shape
class Shape:
    def area(self):
        # Этот метод не имеет конкретной реализации, поскольку содержит оператор pass
        pass

# Определение подкласса Rectangle, наследующего от класса Shape
class Rectangle(Shape):
    def __init__(self, width, height):
        # Инициализация атрибутов width и height
        self.width = width
        self.height = height

    def area(self):
        # Переопределение метода area для расчета площади прямоугольника
        return self.width * self.height

# Определение подкласса Circle, также наследующего от класса Shape
class Circle(Shape):
    def __init__(self, radius):
        # Инициализация атрибута radius
        self.radius = radius

    def area(self):
        # Переопределение метода area для расчета площади круга
        return 3.14 * self.radius * self.radius

# Создание объекта Rectangle
rectangle = Rectangle(5, 10)
# Вычисление и вывод площади прямоугольника
print("Rectangle Area:", rectangle.area())

# Создание объекта Circle
circle = Circle(7)
# Вычисление и вывод площади круга
print("Circle Area:", circle.area())

```
  ### Результат
  ![5](https://github.com/armuane/laba8/blob/main/Desktop/laba8/5.png?raw=true)

 
## Краткий вывод:
Этот код создает иерархию классов для расчета площадей различных форм (прямоугольника и круга). Каждый подкласс (Rectangle и Circle) наследует метод area от базового класса Shape и переопределяет его, чтобы предоставить конкретную реализацию для каждой формы. Затем создаются объекты каждого подкласса, и их методы area вызываются для расчета и вывода площадей.


   


# Самостоятельные работы
   ## Самотоятельная работа 1


  ```python
class Animal:
    def __init__(self, species, sound):

        self.species = species
        self.sound = sound

    def make_sound(self):

        print(f"The {self.species} makes a {self.sound}!")


lion = Animal("Lion", "roar")


lion.make_sound()
```
  ### Результат
  ![6](https://github.com/armuane/laba8/blob/main/Desktop/laba8/6.png?raw=true)

 
## Краткий вывод:
В данном случае, класс Animal представляет различных животных. Конструктор класса принимает два аргумента - species (вид животного) и sound (звук, который оно издает). У класса есть метод make_sound, который выводит звук, издаваемый животным.

После этого создается объект lion (львица) с видом "Lion" и звуком "roar", и вызывается метод make_sound для вывода соответствующего сообщения.

  ## Самотоятельная работа 2


  ```python
class Animal:
    def __init__(self, species, sound, color):

        self.species = species
        self.sound = sound
        self.color = color

    def make_sound(self):

        print(f"The {self.species} makes a {self.sound}!")

    def introduce(self):

        print(f"I am a {self.color} {self.species}. Listen to my {self.sound}!")


lion = Animal("Lion", "roar", "golden")


lion.make_sound()
lion.introduce()
```
  ### Результат
  ![7](https://github.com/armuane/laba8/blob/main/Desktop/laba8/7.png?raw=true)

 
## Краткий вывод:
Теперь класс Animal имеет дополнительный атрибут color и метод introduce, который представляет животное, указывая его вид, цвет и издаваемый звук.
  ## Самотоятельная работа 3


  ```python
class WildAnimal(Animal):
    def __init__(self, species, sound, color, habitat):
        
        super().__init__(species, sound, color)
        self.habitat = habitat

    def describe_habitat(self):
      
        print(f"I live in the {self.habitat}.")


wild_lion = WildAnimal("Lion", "roar", "golden", "African savannah")


wild_lion.make_sound()
wild_lion.introduce()
wild_lion.describe_habitat()
```
  ### Результат
  ![8](https://github.com/armuane/laba8/blob/main/Desktop/laba8/8.png?raw=true)

 
## Краткий вывод:
Теперь у нас есть подкласс WildAnimal, который наследует от Animal. Он добавляет новый атрибут habitat (место обитания) и метод describe_habitat, который выводит информацию о месте обитания.

  ## Самотоятельная работа 4


  ```python
class Animal:
    def __init__(self, species, sound, color):

        self.species = species
        self.__sound = sound
        self.color = color

    def make_sound(self):

        print(f"The {self.species} makes a {self.__sound}!")

    def introduce(self):

        print(f"I am a {self.color} {self.species}. Listen to my {self.__sound}!")

    def get_sound(self):

        return self.__sound

    def set_sound(self, new_sound):

        self.__sound = new_sound


lion = Animal("Lion", "roar", "golden")


lion.make_sound()
lion.introduce()


current_sound = lion.get_sound()
print(f"Current sound of the Lion: {current_sound}")


lion.set_sound("growl")


lion.make_sound()
lion.introduce()
```
  ### Результат
  ![9](https://github.com/armuane/laba8/blob/main/Desktop/laba8/8.png?raw=true)

 
## Краткий вывод:
В этой версии кода атрибут sound инкапсулирован, делая его приватным (__sound). Добавлены методы get_sound и set_sound для получения и установки значения этого атрибута соответственно.

  ## Самотоятельная работа 5


  ```python
class Pet:
    def make_sound(self):

        pass


class Dog(Pet):
    def make_sound(self):

        print("Woof! Woof!")


class Cat(Pet):
    def make_sound(self):

        print("Meow! Meow!")


my_dog = Dog()
my_cat = Cat()


my_dog.make_sound()
my_cat.make_sound()
```
  ### Результат
  ![10](https://github.com/armuane/laba8/blob/main/Desktop/laba8/10.png?raw=true)
  ## Краткий вывод:
  В этом примере мы создали базовый класс Pet, который содержит метод make_sound, а затем определили два подкласса: Dog и Cat, которые наследуют от Pet и переопределяют метод make_sound для представления звука собаки и кошки соответственно.
  # Общий вывод:
  Введение в объектно-ориентированное программирование (ООП) представляет собой ключевой аспект в разработке программного обеспечения, который позволяет структурировать код вокруг объектов, представляющих реальные сущности, а также использовать концепции наследования, инкапсуляции и полиморфизма для создания более гибкого и понятного кода.

ООП базируется на следующих принципах:

Инкапсуляция: Скрывает внутреннюю реализацию объектов и предоставляет интерфейс для их взаимодействия. Атрибуты и методы объединяются в классы, что облегчает поддержку кода и сокрытие деталей реализации.

Наследование: Позволяет создавать новые классы на основе существующих, наследуя их атрибуты и методы. Это снижает дублирование кода и улучшает структуру программы.

Полиморфизм: Объекты разных классов могут обладать одинаковым интерфейсом, что позволяет использовать их взаимозаменяемо. Полиморфизм упрощает кодирование и повышает его гибкость.

ООП применяется для более эффективной организации кода, улучшения его читаемости, уменьшения сложности программ и обеспечения повторного использования кода. Он позволяет моделировать реальные объекты и их взаимодействие, что делает разработку программ более интуитивной и эффективной.
