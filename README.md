# Решение задачи классификации на датасете Iris Dataset

## Описание проекта

Это репозиторий моего решения задачи классификации на известном датасете **Iris Dataset**! Этот проект демонстрирует применение различных методов машинного обучения для классификации видов ирисов на основе их морфологических характеристик. Датасет Iris является одним из самых популярных и часто используемых в машинном обучении, что делает его отличной отправной точкой для демонстрации навыков анализа данных и построения моделей.

### Ссылки на источники
- [Iris Dataset на Kaggle](https://www.kaggle.com/competitions/spaceship-titanic)
- [Описание датасета на GeeksforGeeks](https://www.geeksforgeeks.org/iris-dataset/)
- [Scikit-learn документация по Iris Dataset](https://scikit-learn.org/1.5/auto_examples/datasets/plot_iris_dataset.html)

## О датасете Iris

Датасет Iris, также известный как Fisher's Iris Dataset, был впервые представлен британским биологом и статистиком Рональдом Фишером в 1936 году. Он состоит из 150 образцов ирисов, разделенных на три вида:
- **Iris setosa**
- **Iris versicolor**
- **Iris virginica**

Каждый образец характеризуется четырьмя признаками:
- Длина чашелистика (sepal length)
- Ширина чашелистика (sepal width)
- Длина лепестка (petal length)
- Ширина лепестка (petal width)

Эти признаки измеряются в сантиметрах и используются для классификации цветков на один из трех видов. Датасет является классическим примером для задач классификации и кластеризации в машинном обучении.

## Решение задачи

### Используемые инструменты и технологии
- **Python** — основной язык программирования.
- **Pandas** — для обработки и анализа данных.
- **Matplotlib и Seaborn** — для визуализации данных.
- **Scikit-learn** — для построения и оценки моделей машинного обучения.
- **Методы классификации**:
  - Логистическая регрессия (`LogisticRegression`)
  - Метод k-ближайших соседей (`KNeighborsClassifier`)
  - Метод опорных векторов (`SVC`)
  - Случайный лес (`RandomForestClassifier`)

### Основные шаги решения
1. **Загрузка и предобработка данных**:
   - Датасет был загружен с использованием функции `load_iris` из библиотеки `sklearn.datasets`.
   - Данные были преобразованы в DataFrame для удобства анализа.
   - Проведена проверка на наличие пропущенных значений и анализ распределения признаков.

2. **Визуализация данных**:
   - Построены гистограммы распределения признаков.
   - Созданы парные графики для анализа взаимосвязей между признаками.
   - Построены boxplot для каждого признака в разрезе видов ирисов.
   - Построена тепловая карта корреляции между признаками.

3. **Подготовка данных для обучения**:
   - Признаки были масштабированы с использованием `StandardScaler`.
   - Целевая переменная (вид ириса) была закодирована с помощью `LabelEncoder`.
   - Данные были разделены на обучающую и тестовую выборки в соотношении 70:30.

4. **Обучение и оценка моделей**:
   - Были обучены четыре модели: логистическая регрессия, метод k-ближайших соседей, метод опорных векторов и случайный лес.
   - Для каждой модели были рассчитаны метрики точности, полноты и F1-меры, а также построены матрицы ошибок.

### Результаты
Все модели показали **100% точность** на тестовой выборке, что свидетельствует о высокой предсказательной способности моделей на данном датасете. Это связано с тем, что датасет Iris хорошо разделим, особенно вид Iris setosa, который линейно отделим от двух других видов.
