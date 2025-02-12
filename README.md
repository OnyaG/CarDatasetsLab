# ПСИАПД
# Отчет по 1 лабораторной

## Содержание
---
1. [Теоретическая база](#теоретическая-база)
2. [Описание разработанной системы (алгоритмы, принципы работы, архитектура)](#[описание-разработанной-системы])
3. [Результаты работы и тестирования системы (скриншоты, изображения, графики, закономерности)](#[результаты-работы-и-тестирования-системы])
4. [Выводы по работе](#[выводы-по-работе])
5. [Использованные источники](#[использованные-источники])
---
## Теоретическая база
### Сверточные нейронные сети
Сверточные нейронные сети (Convolutional Neural Networks, CNN) – класс алгоритмов машинного обучения. С их помощью удается достичь впечатляющих результатов в области распознавания образов, классификации изображений, а также обработки и анализа видеоданных.
В состав сверточной нейронной сети входит несколько слоев. От количества слоев зависит мощность архитектуры и эффективность обучения. 
#### Схема основных составляющих свёрточной нейронной сети:
- сверточный слой;
- пулинг;
- нормализация по батчу;
- полносвязный слой.
---
В процессе **свертки** нейронная сеть удаляет ненужное и оставляет полезное, т.е. то, что нужно для анализа изображения. В качестве примера можно привести линии, края и плоские области. **Свертка** может быть создана **для каждого признака**. Нейронная сеть сама подбирает их, когда выполняет распознавание и классификацию в каждом слое свертки.

Следующим после слоя свертки идет **слой пулинга**. В нем **из признаков**, отобранных **слоем свертки**, выбираются наиболее **важные** и удаляются несущественные. **Слой свертки** может быть снова применен к результатам, полученным в процессе пулинга, и **повторен несколько раз**. Это необходимо для построения иерархии признаков, начиная с самых **примитивных** (фрагменты контуров) и заканчивая **сложными** (кошачьи глаза или форма ушей).

**Задача первых слоев** сверточной нейронной сети – **анализ мельчайших элементов изображения** (ворсинки, трещинки и т.д.), размер которого может составлять 2 x 2 или 3 x 3 пикселя. Такой маленький формат не позволяет определить глаза или уши кошки или деревья, на которых она сидит. Однако можно найти различия в цвете и свете – грани между различными объектами. **Для следующих слоев характерны сложные объекты**, такие как круги и другие фигуры.

Пакетный слой (**батч**) (англ. batch gradient descent) — реализация **градиентного спуска**, когда на каждой итерации обучающая выборка просматривается целиком, и только после этого изменяются веса модели.

В **полносвязных слоях** каждый нейрон соединён со всеми нейронами предыдущего слоя. Полносвязные слои обычно используются **в конце сети** для **преобразования признаков**, извлечённых предыдущими слоями, в **окончательные результаты**. Например, в задаче классификации изображений полносвязные слои могут преобразовывать признаки объекта (формы и текстуры) в выводы о принадлежности изображения к тому или иному классу объектов.

---
### ResNet
ResNet — это сокращенное название для Residual Network (дословно  — «остаточная сеть»).
При увеличении "плоских" слоев в стиле VGG качество сети падает, а не растет (даже на обучающей выборке, не говоря уже о тестовой). При большой глубине НС возникает проблема затухающего градиента, таким образом, сеть перестает обучаться. 


## Описание разработанной системы
---
## Результаты работы и тестирования системы
---
## Выводы по работе
---
## Использованные источники
- [Сверточные нейронные сети](https://gb.ru/blog/svertochnye-nejronnye-seti)
- [Типы слоёв нейронной сети](https://aisec.cs.msu.ru/section_robust_ml/nn_architectures/)
- [Архитектуры нейронных сетей](https://aisec.cs.msu.ru/section_robust_ml/nn_architectures/)
- [ResNet](https://neurohive.io/ru/vidy-nejrosetej/resnet-34-50-101/)
