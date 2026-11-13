# Mixer

Локальные модели, которые пишут моды, рендер и миксины для Minecraft на Java под нужную версию игры.

- Сайт: https://ma3stro567.github.io/mixer/
- Модели: `Mixer-0.5B-Q8_0.gguf` и `Mixer-0.6B-v2-Q8_0.gguf` в Releases этого репозитория.
- Таблицы результатов: папка `data/` (CSV).

## Запуск

```
llama-server -m Mixer-0.5B-Q8_0.gguf -ngl 99 -c 8192 --jinja --temp 0.2 --repeat-penalty 1.1
```

Первая строка системного промпта — цель: `[MC=1.21.4][LOADER=fabric][MAP=yarn][JAVA=21]`.

Проверки автоматические, без ИИ-судьи: синтаксис Java, реальные импорты, утечки версий, якоря;
HumanEval-Java (MultiPL-E) — компиляция и тесты.
