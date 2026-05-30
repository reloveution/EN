---
name: english-exercise-check
description: >-
  Checks user answers to English grammar exercises: mandatory literal Russian
  gloss plus natural Russian translation, then target tense/voice, errors,
  and short idiom notes. Use when the user says "проверь ответ", pastes a line
  from translate.txt or tense drills, or asks about verb forms.
disable-model-invocation: true
---

# English exercise answer check

## When to use

- Пользователь прислал **свой вариант** английского по строке из `translate.txt`, `05-tenses`, `*exc*` и т.п.
- Просьбы: «проверь», «правильно ли», «какое время», «разбор ошибок».

## What to do

Следуй правилу проекта: `.cursor/rules/english-exercise-check-review.mdc` (порядок блоков: **дословно + нормальный перевод оба обязательны**, идиомы).

**Краткий шаблон ответа (пример структуры):**

```text
Дословно: …
По-русски (нормально): …

Нужно в EN: … (время, залог).

Твой вариант: верно / нет; правки: …

Идиомы: … — букв.: …; по смыслу: …
```

Если идиом нет — строку «Идиомы:» опусти. Строки «Дословно:» и «По-русски (нормально):» **не опускать**.

## Связь с генерацией

Лексика при **составлении** новых заданий — `.cursor/rules/english-exercise-generation.mdc`. Этот скилл — только **проверка ответов**.
