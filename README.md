# ba-claude-skills

Набор skills для [Claude Code](https://docs.claude.com/en/docs/claude-code/overview) и Claude Agent SDK, ориентированных на задачи **бизнес-аналитика**: подготовка требований, вариантов использования, работа со стейкхолдерами.

## Состав

| Skill | Назначение |
|-------|------------|
| [`skills/use-case`](skills/use-case/SKILL.md) | Составление требований в формате **Вариант использования (Use Case)** по методологии Алистера Коберна. Включает строгие правила оформления основного сценария, расширений (с отдельными подшагами для исходов), таблиц FR/NFR и генерации `.docx`. |

## Установка

### Claude Code (локально)

1. Клонируй репозиторий в любое удобное место:
   ```bash
   git clone https://github.com/Qloker/ba-claude-skills.git
   ```
2. Скопируй нужный skill в директорию skills Claude Code:
   - Windows: `%APPDATA%\Claude\skills\`
   - macOS / Linux: `~/.claude/skills/`

   Пример (Windows PowerShell):
   ```powershell
   Copy-Item -Recurse .\ba-claude-skills\skills\use-case "$env:APPDATA\Claude\skills\"
   ```
3. Перезапусти Claude Code. Skill станет доступен для вызова через `Skill` tool.

### Через плагин

Skills также могут подключаться через плагиновую систему Claude Code. Подробнее — в документации: https://docs.claude.com/en/docs/claude-code/plugins

## Быстрый старт с `use-case`

Попроси Claude Code:
> «Опиши вариант использования: снять наличные в банкомате»

Или явно:
> «Используй skill use-case и составь ВИ: оператор квитирует аварийное событие на мнемосхеме»

Skill развернёт полное описание из 13 полей (по Коберну) + сгенерирует `.docx` с таблицами функциональных и нефункциональных требований.

## Лицензия

MIT
