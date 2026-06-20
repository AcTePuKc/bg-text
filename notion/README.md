# bg-text for Notion

Use `bg-text` with Notion in two ways:

1. as a standalone Notion AI skill
2. through an MCP-enabled assistant that can read and edit Notion pages

## Option A: Notion AI Skill

This is the simplest setup. It works as a compact prompt that turns Notion AI into a Bulgarian text quality assistant.

### Setup

1. Open [`bg-text-notion-skill.md`](bg-text-notion-skill.md)
2. Copy the full content
3. Create a new page in Notion
4. Paste the Markdown into the page
5. Open the page menu and choose **Use with AI** → **Use as AI skill**
6. Name the skill `bg-text`

### Usage

1. Select text in a Notion page
2. Click **Ask AI**
3. Choose the `bg-text` skill
4. Ask for a correction, rewrite, or review

### What the standalone skill includes

- condensed typography rules
- weak wording and anti-pattern checks
- UI/localization guidance
- a short final quality checklist

Use this option when you want a lightweight review directly inside Notion.

## Option B: Notion Through MCP

Use the full repository with any assistant or client that supports:

- local skills or prompt files
- the official Notion MCP server or an equivalent Notion connector

This path gives you the full `bg-text` structure, including domain references, scoring, and progressive loading.

### Setup

1. Use this repository in your preferred client
2. Connect the Notion MCP server: [Notion MCP guide](https://developers.notion.com/guides/mcp/get-started-with-mcp)
3. Grant the client access to the relevant pages

### Example prompts

```text
Read my Notion page "Landing copy" and apply bg-text rules.
Fix typography, remove weak wording, and suggest a cleaner version.
```

```text
Score the text quality of my Notion page "About us" with bg-text.
```

### Suitable clients

- Claude Code
- Codex
- Gemini
- Cursor
- OpenClaw
- other assistants that can use local prompt files and a Notion connector

### Notes

- The standalone Notion skill is shorter by design.
- The repository version is broader and easier to maintain.
- Some Notion UI labels remain in English because they follow Notion's product interface.

---

# bg-text за Notion

Можете да използвате `bg-text` с Notion по два начина:

1. като самостоятелно Notion AI умение
2. чрез агент или клиент с MCP достъп до Notion

## Вариант А: Notion AI умение

Това е най-лесният вариант. Представлява стегнат prompt, който превръща Notion AI в помощник за качество на български текст.

### Настройка

1. Отворете [`bg-text-notion-skill.md`](bg-text-notion-skill.md)
2. Копирайте цялото съдържание
3. Създайте нова страница в Notion
4. Поставете Markdown съдържанието в страницата
5. Отворете менюто на страницата и изберете **Use with AI** → **Use as AI skill**
6. Назовете умението `bg-text`

### Използване

1. Маркирайте текст в страница на Notion
2. Натиснете **Ask AI**
3. Изберете умението `bg-text`
4. Поискайте корекция, пренаписване или преглед

### Какво включва самостоятелното умение

- съкратени правила за типография
- проверки за слаби конструкции и антишаблони
- насоки за UI и локализация
- кратък финален контролен списък

Използвайте този вариант, ако искате лек и бърз преглед директно в Notion.

## Вариант Б: Notion чрез MCP

Използвайте цялото хранилище с всеки агент или клиент, който поддържа:

- локални умения или prompt файлове
- официалния Notion MCP сървър или еквивалентен Notion конектор

Това дава достъп до пълната структура на `bg-text`, включително домейнните справки, оценяване и прогресивно зареждане.

### Настройка

1. Използвайте това хранилище в предпочитания от вас клиент
2. Свържете Notion MCP сървъра: [инструкции за Notion MCP](https://developers.notion.com/guides/mcp/get-started-with-mcp)
3. Дайте на клиента достъп до нужните страници

### Примерни заявки

```text
Прочети страницата ми в Notion „Текст за лендинг“ и приложи правилата на bg-text.
Поправи типографията, премахни слабите конструкции и предложи по-ясна версия.
```

```text
Оцени качеството на текста на страницата ми в Notion „За нас“ с bg-text.
```

### Подходящи клиенти

- Claude Code
- Codex
- Gemini
- Cursor
- OpenClaw
- други асистенти, които могат да ползват локални prompt файлове и Notion конектор

### Бележки

- Самостоятелното Notion умение е нарочно по-кратко.
- Версията от хранилището е по-пълна и по-лесна за поддръжка.
- Част от имената в интерфейса остават на английски, защото следват UI на Notion.
