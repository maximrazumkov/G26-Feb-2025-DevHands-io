# G26-Feb-2025-DevHands-io
G26 // Feb-2025 // DevHands.io

# **Расчет количества касс в магазине с учетом конверсии**

## **Дано:**
- **1000 посетителей в день**.
- **Предположим что конверсия 12–15%**:
  - **При 12%**: 120 покупателей в день.
  - **При 15%**: 150 покупателей в день.
- **Среднее время обслуживания на кассе**: **2–3 минуты**.
- **Магазин работает 12 часов в день**.

---

## **Сценарий 1: Дорого, но быстрое обслуживание**
### **Цель:** минимизировать очереди, время ожидания **1–2 минуты**.

- **Одна касса** способна обслуживает **20-30 клиентов в час** (если на клиента уходит 2-3 минуты). Считаем по худшему сценарию
- Число касс при разной конверсии:
  - **При 12% (120 покупателей)**:
    - 120 / (30 * 12) = 0.33 → **Минимально 1 касса**.
  - **При 15% (150 покупателей)**:
    - 150 / (30 * 12) = 0.42 → **Минимально 1 касса, но с риском очередей в часы пик**.
- **Оптимальный вариант**: **2 кассы**, чтобы избегать перегрузок в пиковые часы и пиковые дни. Обычно в выходные происходит скачок проходимости в среднем в 2 раза

---

## **Сценарий 2: Дешевле, но клиенты будут ждать дольше**
### **Цель:** минимизировать расходы, допустимая очередь **3–5 минут**.

- Если время обслуживания **3 минуты**, одна касса пропускает **20 клиентов в час**.
- Число касс при разной конверсии:
  - **При 12% (120 покупателей)**:
    - 120 / (20 * 12) = 0.5 → **Минимально 1 касса**, но возможны очереди.
  - **При 15% (150 покупателей)**:
    - 150 / (20 * 12) = 0.625 → **Минимально 1 касса, но очереди в часы пик**.
- **Выбор**:
  - **1 касса** → дешевле, но возможны ожидания **5+ минут** в вечерний час пик или выходные дни.
  - **2 кассы** → лучшее решение, чтобы минимизировать очереди.

---

## **Вывод:**
- **Минимальный вариант**: 1 касса (но очереди в вечернее время и выходные дни).
- **Оптимальный вариант**: 2 кассы (избегаем задержек).
- **Дополнительный резерв**: если ожидается рост продаж, оставить место для **3-й кассы**.


------------------------------------------------------------------------------

# **Рассчет кол-ва лифтов в небоскребе**

## **Дано:**
- **30 этажей**.
- **3 входные группы (подъезда)**:
  - **Всего сотрудников в здании**: 30×300=9000 человека
  - **Каждый подъезд обслуживает**: 9000/3=3000 человек
- **Каждый этаж = 300 человек.**.
- **Допустим средняя вместимость лифта: 15 человек**.
- **Среднее время поездки (включая остановки и возврат): 3 минуты (180 секунд).**.
- **Часы пик:  допустим 80% сотрудников перемещаются за 2 часа.**.

---

## **Шаг 1: Определяем необходимую пропускную способность**

  - **В час пик нужно перевезти 80% от 3000 человек в каждом подъезде:**:
    - 3000×0.8=2400 человек за 2 часа
  - **Значит, нужно перевозить 1200 человек в час (в каждом подъезде). Это **:
    - 1200/15=80 → **поездок в час**.
  - **Каждый лифт делает: **:
    - 60/3=20 → **поездок в час**.
  - **Исходя из предыдущего примеро минимум нужно: **:
    - 80/20=4 → **лифтов нужно**.
      
## **Шаг 2: Добавляем запас на перегрузки и ожидание**, чтобы избегать перегрузок в пиковые часы
  - В реальности лифты редко загружаются идеально (иногда уезжают полупустыми или часть лифтов может не работать). Поэтому добавляем запас +40%, чтобы избежать длинных очередей
  - Число касс при разной конверсии:
    - **При 12% (120 покупателей)**:
      - 4×1.4=5.6 → **если округлять, то 6 лифтов**.
---

## **Вывод:**
- **Минимальный вариант** → 4 лифта на подъезд (12 всего) (очереди возможны в часы пик)..
- **Оптимальный вариант** → 6 лифтов на подъезд (18 всего) (минимальные ожидания)..
- **Дополнительный резерв**: 8 лифтов на подъезд (24 всего) (быстрое обслуживание даже при высокой загруженности или при некоторым кол-ве неработующих лифтов)..
