# Challenge - Catboost Regression 🐆

## 📌 Описание проекта

Этот проект посвящен решению задачи регрессии для предсказания цен на недвижимость в Мельбурне. Работа выполнялась в рамках учебного соревнования по Data Science *(курс Глеба Михайлова на Stepik)*.  
  
Основной алгоритм: **CatBoostRegressor**.  

Метрика качества: MAPE *(Mean Absolute Percentage Error)* – средняя абсолютная ошибка в процентах.  

## 📊 Данные

- Источник данных: Цены на недвижимость в Мельбурне.
  
- Каждая строка представляет объект недвижимости с различными характеристиками.
  
- Данные содержат пропущенные значения и выбросы, которые обрабатываются перед обучением модели.

## 🔍 Основные этапы работы

### 1. Разведочный анализ данных (EDA)

- Анализ распределения цен и признаков.

- Выявление выбросов и аномалий.

- Обработка пропущенных значений.

### 2. Подготовка данных

- Кодирование категориальных признаков.

- Разбиение на обучающую и тестовую выборку.

- Нормализация и масштабирование данных.

### 3. Обучение модели

- Используется **CatBoostRegressor** – мощный градиентный бустинг по деревьям решений.

- Подбор гиперпараметров для улучшения качества предсказаний.

- Оценка модели на тестовых данных по метрике **MAPE**.

### 4. Анализ результатов

- Визуализация ошибок модели.

- Интерпретация важности признаков с помощью **SHAP**.

## 🏁 Выводы

Проект демонстрирует, как можно эффективно использовать CatBoost для предсказания цен на недвижимость. Были проанализированы и обработаны данные, настроена модель, проведена оценка качества предсказаний, а также интерпретация её решений с помощью SHAP.

---

📌 **Автор:** Ivan4956

