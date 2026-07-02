# 🗂️ Карта Figma-скилов

Набор Figma-скилов для AI-агентов (Claude Code) из [Figma Community](https://www.figma.com/community/skills) — что делает каждый, **когда звать** и как они связаны.

**17 скилов · 6 официальных Figma + 11 community · 5 групп.** Установлены в `~/.claude/skills`.

> 🌐 **Живая дизайн-версия:** https://mmkeewa.github.io/figma-skills-map/

---

## 1. Генерация и правка макетов

| Скил | Что делает | Когда звать | Автор |
|---|---|---|---|
| [`figma-generate-design`](https://developers.figma.com/docs/figma-mcp-server/skill-figma-generate-design/) `Figma` | Собирает новые экраны из **существующих** компонентов и переменных дизайн-системы | «собери экран из ДС», «запушь страницу в Figma» | Figma |
| [`edit-figma-design`](https://github.com/warpdotdev/figma-skills/tree/main/.agents/.skills/edit-figma-design) | Рисует/правит дизайн **из текстового описания** — мокап, вайрфрейм, флоу. Может стартовать с чистого файла | «нарисуй мокап по описанию», «вайрфрейм в Figma» | Warp |
| [`prototype-to-figma`](https://github.com/alima-max/prototype-to-figma-skill) | Разбирает код-прототип на фреймы по флоу, кладёт компоненты ДС и аннотирует взаимодействия | «прототип → Figma», «handoff из кода» | alima-max |
| [`figma-generate-library`](https://developers.figma.com/docs/figma-mcp-server/skill-figma-generate-library/) `Figma` | Строит компоненты и библиотеку в Figma **из кодовой базы** | «собери компоненты из кода», «построй библиотеку» | Figma |

## 2. FigJam, Slides, диаграммы и планы

| Скил | Что делает | Когда звать | Автор |
|---|---|---|---|
| [`figma-use-figjam`](https://developers.figma.com/docs/figma-mcp-server/skill-figma-use-figjam/) `Figma` | Контент FigJam: стикеры, секции, коннекторы, таблицы, code-блоки | «набросай доску в FigJam» | Figma |
| [`figma-use-slides`](https://developers.figma.com/docs/figma-mcp-server/skill-figma-use-slides/) `Figma` | Создаёт и правит презентации в Figma Slides с сохранением стилей | «презентация в Figma Slides», «поправь слайды» | Figma |
| [`figma-generate-diagram`](https://developers.figma.com/docs/figma-mcp-server/skill-figma-generate-diagram/) `Figma` | Диаграммы в FigJam: архитектура, ERD, флоучарты, sequence, state | «нарисуй архитектуру», «ERD / флоучарт» | Figma |
| [`generate-project-plan`](https://github.com/figma/mcp-server-guide/tree/main/workflow-skills/generate-project-plan) `Figma` | Из PRD + контекста кода собирает **интерактивную** доску-план проекта в FigJam | «project plan из PRD», «план проекта в FigJam» | Figma |

## 3. Дизайн-система и spacing

| Скил | Что делает | Когда звать | Автор |
|---|---|---|---|
| [`apply-design-system`](https://github.com/edenspiekermann/Skills/tree/main/skills/apply-design-system) | Связывает существующий дизайн с компонентами дизайн-системы | «привяжи к ДС», «свяжи с компонентами» | Edenspiekermann |
| [`audit-design-system`](https://github.com/edenspiekermann/Skills/tree/main/skills/audit-design-system) | Аудит на «дрейф» от ДС: недостающие shared-компоненты, оверрайды, непривязанные токены → `fix` | «проверь на дрейф от ДС», «где отвязанные токены» | Edenspiekermann |
| [`fix-design-system-finding`](https://github.com/edenspiekermann/Skills/tree/main/skills/fix-design-system-finding) | Чинит конкретную находку из аудита ← `audit` | «почини находку», «убери оверрайд» | Edenspiekermann |
| [`rad-spacing`](https://github.com/nolanperk/rad-spacing) | Иерархические отступы по Gestalt: внешним контейнерам больше воздуха. Кратно 8/4px | «расставь отступы по иерархии», «наведи spacing» | Nolan Perkins |

## 4. Токены и контракты

| Скил | Что делает | Когда звать | Автор |
|---|---|---|---|
| [`cc-figma-tokens`](https://github.com/nvillapiano/component-contracts-figma/tree/main/skills/cc-figma-tokens) | Строит Figma-переменные (Primitives + Semantic) из токен-файлов. **Пререквизит** → `cc-figma-component` | «залей токены в Figma», «переменные из токенов» | Nick Villapiano |
| [`cc-figma-component`](https://github.com/nvillapiano/component-contracts-figma/tree/main/skills/cc-figma-component) | Собирает Figma-компонент со всеми вариантами из контракта ← `cc-figma-tokens` | «собери компонент из контракта», «варианты в Figma» | Nick Villapiano |
| [`sync-figma-token`](https://github.com/firebenders/sync-figma-token-skill) | Двусторонняя синхронизация токенов код↔Figma с детекцией дрейфа | «синхронизируй токены», «проверь дрейф токенов» | Firebender |

## 5. Спеки, доступность и агенты

| Скил | Что делает | Когда звать | Автор |
|---|---|---|---|
| [`create-voice`](https://github.com/redongreen/uSpec/tree/main/skills/create-voice) | Спека для скринридеров (VoiceOver / TalkBack / ARIA) прямо в Figma. Часть системы uSpec | «спека для скринридера», «VoiceOver / ARIA» | Ian Guisard · uSpec |
| [`figma-augment-parallel`](https://github.com/AugmentedAJ/skills/tree/main/augment-multi-agent-figma) | Гайд по Figma MCP + агенты Augment: реализация дизайнов, параллельные воркфлоу, запись обратно в Figma | «Figma + Augment», «параллельные воркфлоу» | Augment |

---

## Связки и подводные камни

- **Токены → компонент.** Порядок обязателен: `cc-figma-tokens` → `cc-figma-component`. Пока в файле нет коллекций Primitives и Semantic, компонент не соберётся.
- **Аудит → починка.** `audit-design-system` → `fix-design-system-finding`.
- **Три пути «код → Figma».** `figma-generate-design` (по ДС) · `edit-figma-design` (из текста) · `prototype-to-figma` (из прототипа) · `figma-generate-library` (компоненты).
- **`/multi-agent` зовётся иначе.** На карточке Figma Community это `/multi-agent`, но внутреннее имя скила — `figma-augment-parallel`. Вызывать по нему.
- **`create-voice` — часть uSpec.** Умеет рендерить a11y-спеку, но на вход хочет component-`.md` из системы uSpec. Полный набор: `npx uspec-skills init`.
- **Две синхронизации токенов.** `sync-figma-token` — двусторонняя код↔Figma с дрейфом; `cc-figma-tokens` — генерация из контракта в одну сторону.

---

## Установка скила

Community-скилы ставятся копированием папки скила в `~/.claude/skills/`:

```bash
git clone --depth 1 https://github.com/<author>/<repo> /tmp/skill-src
cp -R /tmp/skill-src/<path-to-skill-folder> ~/.claude/skills/<skill-name>
```

Официальные `Figma`-скилы идут в комплекте с плагином Figma MCP.

---

*Источник карточек: [Figma Community · Skills](https://www.figma.com/community/skills). Ссылки в таблице ведут в репозитории авторов.*
