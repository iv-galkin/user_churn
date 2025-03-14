# User Churn Prediction (предсказание оттока пользователей)

## Описание

В данном проекте я работаю с данными о пользователях, чтобы предсказать их отток (churn). Это задача бинарной классификации, где целевая переменная `Churn` принимает значения 0 (пользователь остался) или 1 (пользователь ушел). Этот проект является учебным, однако такая задача актуальна для бизнеса, так как позволяет компаниям выявлять клиентов, которые могут прекратить использование услуг. Правильное предсказание позволяет разработать стратегии удержания, улучшить качество обслуживания и повысить лояльность.

**Задачи проекта**:
- Предобработка данных:
  - Обработка пропущенных значений.
  - Преобразование типов данных.
  - Удаление дубликатов.
  - Нормализация числовых признаков.
  - Кодирование категориальных признаков.
- Анализ данных:
  - Исследование распределения целевой переменной.
  - Визуализация числовых и категориальных признаков.
  - Построение матрицы корреляций.
- Обучение моделей:
  - Применение линейных моделей (Logistic Regression).
  - Применение моделей градиентного бустинга (CatBoost).
  - Сравнение качества моделей по метрике ROC-AUC.
- Оптимизация гиперпараметров:
  - Поиск оптимальных значений `n_estimators` и `learning_rate` для CatBoost с помощью GridSearchCV.

---

## Подробнее

[Посмотреть ноутбук можно здесь](user_churn_prediction.ipynb)

---

## Используемые библиотеки и методы анализа

### Библиотеки:
- **pandas**, **numpy** – обработка и анализ данных.
- **matplotlib**, **seaborn** – визуализация данных.
- **scikit-learn** – обучение моделей, кросс-валидация, метрики качества.
- **catboost** – обучение моделей градиентного бустинга.

### Методы анализа:
- **Исследовательский анализ данных (EDA)**:
  - Визуализация распределения целевой переменной.
  - Построение гистограмм и boxplot для числовых признаков.
  - Построение круговых диаграмм для категориальных признаков.
  - Построение матрицы корреляций.
- **Машинное обучение**:
  - Линейные модели: LogisticRegressionCV.
  - Градиентный бустинг: CatBoostClassifier.
  - Оптимизация гиперпараметров с помощью GridSearchCV.

---

## Основные результаты
- Лучше всего себя показала модель LogisticRegressionCV, обученная на предобработанных данных, которая показала ROC-AUC = 0.8384 на валидационной выборке.
- Модель CatBoostClassifier также показала хорошее качество (ROC-AUC = 0.8278) и может быть использована для дальнейших экспериментов.
- Проведена качественная предобработка данных, включая обработку пропущенных значений, удаление дубликатов и нормализацию признаков.

---

## 🔧 Установка

Для работы с проектом потребуется **Python 3.x** и следующие библиотеки:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn catboost 
