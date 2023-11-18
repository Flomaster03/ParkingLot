1_1

Описание
Парковки – городская необходимость. Они предоставляют места, где вы можете оставить свой автомобиль, не беспокоясь о том, что его украдут или отбуксируют. Современные системы парковки автомобилей автоматизированы и способны к самоуправлению. В этом проекте вы создадите аналогичную систему, но в упрощенном виде.

Начнем с написания программы, которая сможет поставить вашу машину на парковку и освободить ее, когда машина уедет. Это будет «скелет» нашей функциональной парковки, и мы добавим к нему следующие шаги. В часы пик на парковке могут закончиться свободные места. Программа предоставит нам агрегированную информацию о текущем состоянии лота.

На этом этапе мы напечатаем цвет автомобиля, когда он паркуется, уезжает или прибывает. Цвета для этих строк мы получим из консоли. Например, если цвет автомобиля в каждом случае красный, выходные данные будут Red card has parked, Red car left the parking lotи Red card just parked here.

Пример
Символ > представляет ввод пользователя. Обратите внимание, что это не часть ввода.

Выведите три строки, используя ввод цвета автомобиля с консоли, как показано в примере ниже.

> White
White car has parked.
> Yellow
Yellow car left the parking lot.
> Green
Green car just parked here.


2_5

Описание
На данном этапе наша минималистичная парковка имеет два парковочных места. Предположим, что первое место занято , а второе свободно.

Парковка должна позволять пользователю парковать автомобиль. Это реализуется с помощью parkкоманды. После того, как пользователь ввел эту команду, следует указать регистрационный номер и цвет автомобиля. Например, park KA-01-HH-1234 Blue. Регистрационный номер не должен содержать пробелов. Цвет можно писать как прописными, так и строчными буквами.

Поскольку первое место уже занято, программа должна выделить второе место и напечатать: Blue car parked in spot 2.Цвет должен соответствовать тому, что вводит пользователь.

Чтобы забрать автомобиль, пользователю необходимо напечатать команду, leaveа затем номер парковочного места, например, leave 1. Если в данном месте нет автомобиля, программа должна вывести ошибку: There is no car in spot 1.В противном случае она должна уведомить пользователя о том, что место теперь доступно:Spot 1 is free.

Примеры
Символ > представляет ввод пользователя. Обратите внимание, что это не часть ввода.

Пример 1:

> park KA-01-HH-1234 Blue
Blue car parked in spot 2.
Пример 2:

> leave 1
Spot 1 is free.
Пример 3:

> leave 2
There is no car in spot 2.


3_5

Описание
Для парковки двух мест недостаточно, поэтому давайте увеличим количество парковочных мест. Мы перейдем сразу к 20 местам, пронумерованным от 1 до 20. Изначально все места вакантны.

Когда пользователь хочет припарковать автомобиль, программа должна найти доступное парковочное место с наименьшим номером.

Пользователь может писать команды park , а также leave несколько раз и печатать exit, чтобы завершить программу.

Если парковка заполнена и мест нет, программа должна ввести Sorry, the parking lot is full..

Если для автомобиля доступно несколько мест, программа всегда должна назначить место с наименьшим номером.

Пример
Символ > представляет ввод пользователя. Обратите внимание, что это не часть ввода.

> park KA-01-HH-9999 White
White car parked in spot 1.
> park KA-01-HH-3672 Green
Green car parked in spot 2.
...

> park Rs-P-N-21 Red
Sorry, the parking lot is full.
> leave 1
Spot 1 is free.
> park Rs-P-N-21 Red
Red car parked in spot 1.
> exit


4_5

Описание
В реальной жизни парковки различаются по размеру. На этом этапе мы научимся лучше подражать искусству жизни. Для этого мы сделаем нашу программу настраиваемой, добавив команду create, позволяющую пользователю указывать количество мест. Например, команда create 3делает парковку на три места. Количество пятен должно быть положительным. Вывод программы должен быть следующим:Created a parking lot with 3 spots.

Другие команды, такие как park или, leave должны возвращать ошибку, Sorry, a parking lot has not been created.пока пользователь не введет create команду. Если пользователь позвонит create еще раз, предыдущее состояние парковки должно быть сброшено.

Также важно отслеживать, какие места какие машины занимают. Для этого добавим statusкоманду, которая печатает все занятые места в порядке возрастания. Для каждого места он должен напечатать номер места, регистрационный номер автомобиля и цвет автомобиля, разделенные пробелами, как в примере ниже. Если занятых мест нет, программа должна вывести:Parking lot is empty.

Пример
Символ > представляет ввод пользователя.

> park KA-01-HH-9999 White
Sorry, a parking lot has not been created.
> create 3
Created a parking lot with 3 spots.
> status
Parking lot is empty.
> park KA-01-HH-9999 White
White car parked in spot 1.
> park KA-01-HH-3672 Green
Green car parked in spot 2.
> park Rs-P-N-21 Red
Red car parked in spot 3.
> leave 2
Spot 2 is free.
> status
1 KA-01-HH-9999 White
3 Rs-P-N-21 Red
> exit


