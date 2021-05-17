## Теория:

Есть в консоли такая интересная команда "cowsay":
```bash 
user@group:~$ cowsay "Я консольная коровка"
 ______________________
< Я консольная коровка >
 ----------------------
        \   ^__^
         \  (oo)\_______
            (__)\       )\/\
                ||----w |
                ||     ||
```

Сегодня, в качестве примера, предлагаю Вам написать такое же небольшое приложение, но в браузере.

В репозитории Вы найдете исходный код и картинку.

Поскольку мы начали изучать классы, то и код написан с использованием классов.

Класс называется *cowsay_class*. В классе есть три свойства:
1. this.node - HTML-элемент, в который будет помещена коровка
1. this.messageAnchor - якорь для текста, координаты из которых будет отображаться окошко с текстом
1. this._text - текст сообщения

Остановимся на свойстве *this._text*. В начале класса, для него прописаны два метода:
1. set text(value) {...} - это сеттер, он срабатывает, когда мы пытаемся изменить заданное свойство; он нужен, поскольку изменение текста необходимо произвести в двух местах - непосредственно в ствойстве *this._text* и в окошке с сообщением
1. get text() {...} - это геттер, срабатывает, когда мы пытаемся получить заданное свойство; нужен, поскольку сеттер без геттера  не живет

В классе четыре метода:
1. constructor(node) - вызывается при создании объекта, задает начальные значения создаваемого объекта, принимает на вход HTML-элемент для размещения коровки
1. addImage() - загружает изображение и размещает его в HTML-элементе
1. addMessage() - создает окошко с сообщением; для окошка используются внешние стили из тэга style
1. cowsay() - меняет текст коровки

В js классы устроены немного проще, чем в остальных языках программирования. На момент этой работы, классы - это просто объекты с полным доступом ко внутренним переменным этого объекта. По логике кода методы *addImage()*, *addMessage()* - приватные и должны быть скрыты от внешнего вызова, однако на практике эти методы можно вызывать из любого места. А вот метод *cowsay()* - публичный.

Все остальное по коду не должно вызвать затруднений.

## Вопросы:
Ответьте на вопросы:
1. что такое addEventListener?
1. что такое constructor?
1. в строке 94 есть присваивание: ***var _this = this;***, какова его роль?
1. каким образом коровка получает сообщение для вывода?
1. что такое сеттер?
1. что такое геттер?

## Задание:

Ваша задача, написать собственный cowsay. Выберите себе любого персонажа (это может быть любая кошечка, собачка или герой мультика, может фильма). И заставьте его говорить необходимые фразы.

## Самостоятельно:

Создайте еще одно свойство для класса, которое будет отвечать за цвет окошка с сообщением.

### Ответы на вопросы и выполненные задания жду на почте!