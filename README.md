# Генерация серий иконок

Скилл `icon-generation` ведёт серию иконок от брифа и референсов до PNG в макете. Агент отвечает по-русски, а промпты для генератора пишет по-английски.

## Подключение

Открой этот репозиторий в Claude Code, Codex или Gemini CLI. Для другого проекта скопируй [папку icon-generation](.agents/skills/icon-generation) целиком в каталог своего агента и открой сессию в проекте.

| Агент | Каталог для папки `icon-generation` | Как запустить |
| --- | --- | --- |
| Claude Code | `.claude/skills/` | `/icon-generation` |
| Codex | `.agents/skills/` | `$icon-generation` |
| Gemini CLI | `.agents/skills/` или `.gemini/skills/` | Напиши «Примени скилл icon-generation». Проверить наличие можно через `/skills list`. |

Для другого клиента с поддержкой Agent Skills помести папку в его каталог скиллов. В обычном чате прикрепи [SKILL.md](.agents/skills/icon-generation/SKILL.md) и [инструкцию по MCP](.agents/skills/icon-generation/references/mcp.md). Попроси агента применить их к брифу. Доступные действия зависят от инструментов клиента.

Документация по подключению. [Claude Code](https://code.claude.com/docs/en/skills), [Codex](https://developers.openai.com/api/reference/cli), [Gemini CLI](https://geminicli.com/docs/cli/skills/).

## Запуск

0. Если стиль ещё не выбран, попроси скилл найти референсы и предложить направления.
1. Запусти `icon-generation` в своём агенте и приложи выбранные референсы. Добавь категории, размер и требования бренда. Можно взять [короткий бриф](examples/brief.md).
2. Выбери удачную сетку и укажи ячейки для клоуз-апов, например R1C2.
3. Подготовь PNG нужного разрешения с прозрачным фоном.
4. Используй серию в проекте и проверь её в рабочем размере.

Агент выполняет доступные шаги сам. Для ручной генерации сетки или клоуз-апов он подготовит английские промпты. Для генерации через Figma MCP нужны доступ к редактируемому файлу и кредиты. Можно также указать подключённый Imagine MCP. Для вставки в Figma приложи ссылку на фрейм.

- [Инструкции скилла](.agents/skills/icon-generation/SKILL.md)
- [Запросы агенту для каждого шага](examples/agent-requests.md)
- [Подключение и возможности Figma MCP](https://developers.figma.com/docs/figma-mcp-server/remote-server-installation/)
