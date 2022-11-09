# Optimization

Рассчеты в ноутбуке, прикрепленном к данному репозиторию, были основаны на следующей статье: https://www.mit.edu/~jaillet/general/quickest-flow-soda15.pdf 

Данный алгоритм неплох, но требует доработок в связи со структурой нашей задачи

### Реализация 

Для того, чтобы реализовать алгоритм, для начала я разбил ребра нашего графа на часовые, чтобы было проще работать с часовой пропускной способностью дороги. Выглядит это примерно так:

![photo_2022-11-09 13 51 28](https://user-images.githubusercontent.com/71625522/200784066-0ba94550-245c-4106-afde-063410632826.jpeg)

(синим цветом подписаны время прохождения ребер, зеленым цветом подписаны индексы ребер, маленькие карандашные числа - пропускные способности ребер, большие карандашные числа - потоки ребр после оптимизации)

Далее я действовал в сторону статьи: так как задача поиска наискорейшего потока сводится к задаче поиска максимального потока в сети, сначала была решена вторая задача методом линейного программирования, затем была аналогично решена первая (отдельно для больших и для маленьких грузовиков соответственно). 
