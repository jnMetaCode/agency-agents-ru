# agency-agents на русском (команда AI-экспертов)

🌐 **Русский** | [English (upstream)](https://github.com/msitarzewski/agency-agents) | [简体中文](https://github.com/jnMetaCode/agency-agents-zh) | [한국어](https://github.com/jnMetaCode/agency-agents-ko) | [Português (BR)](https://github.com/jnMetaCode/agency-agents-pt-BR)

> **187 готовых к использованию AI-агента** — охватывают инжиниринг, дизайн, маркетинг, продукт, игры, безопасность, финансы и ещё 18 отделов. Это не универсальные промпт-шаблоны: у каждого агента собственная персона, профессиональный воркфлоу и чётко определённые артефакты. Поддержка Claude Code / Cursor / Copilot и ещё 17 AI-инструментов для разработки.

Русская community-версия [agency-agents](https://github.com/msitarzewski/agency-agents). Полный перевод 184 апстрим-агентов. **PR приветствуются** для агентов, специфичных для российского рынка (VK / Telegram bot operator / Yandex SEO / Habr / Wildberries / Ozon / Тинькофф-style fintech / соблюдение ФЗ-152 и т.д.).

[![GitHub stars](https://img.shields.io/github/stars/jnMetaCode/agency-agents-ru?style=social)](https://github.com/jnMetaCode/agency-agents-ru)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://makeapullrequest.com)


### 📊 Масштаб проекта

| 🤖 AI-агенты | 🌏 Переводы | 🇷🇺 Российские оригиналы | 🧠 Инструменты | 🏢 Отделы |
|:---:|:---:|:---:|:---:|:---:|
| **187** | **184** | **3** | **17** | **18** |

---

## 🚀 Agency Orchestrator — заставьте библиотеку персон работать по-настоящему

> **💡 Одна фраза — несколько AI-экспертов автоматически кооперируются, законченный результат за минуты.**
>
> Библиотека персон предоставляет специалистов; [**Agency Orchestrator**](https://github.com/jnMetaCode/agency-orchestrator) заставляет их работать как настоящая команда.

```bash
npm install -g agency-orchestrator
ao compose "Напиши глубокий аналитический материал про AI-агентов" --run
```

```
🎭 Автокастинг → Нарратолог + Психолог + Контент-создатель + Нарративный дизайнер
📊 Автооркестрация → DAG-воркфлоу, авто-определение зависимостей, параллельное исполнение
✅ Автодоставка → готовый результат за несколько минут
```

| Возможность | Описание |
|:---|:---|
| 🎯 **Оркестрация без кода** | Естественный язык или YAML, опишите задачу одной фразой |
| ⚡ **Параллельный DAG-запуск** | Авто-определение зависимостей, независимые шаги параллельно — в 2 раза быстрее |
| 🔄 **Возобновление с чекпоинта** | Сбойный шаг перезапускается отдельно — не нужно начинать заново |
| 🆓 **6 бесплатных LLM** | Claude Code / Gemini CLI / Copilot / Codex / OpenClaw / Ollama |
| 💰 **3 API-интеграции** | DeepSeek / Claude API / OpenAI |
| 📋 **32 готовых шаблона** | Разработка, маркетинг, аналитика, дизайн, операционка |

<p align="center">
  <a href="https://github.com/jnMetaCode/agency-orchestrator">
    <strong>⭐ Изучите Agency Orchestrator — задействуйте 187 агента →</strong>
  </a>
</p>

---

## Что это?

Готовая к использованию **библиотека AI-персон**. У каждого агента чёткая идентичность, критические правила, рабочий процесс и определённые артефакты. Установите в свой AI-инструмент и активируйте на естественном языке.

**Отличие от обычных промптов**: обычные промпты говорят AI «ты — эксперт»; здесь же агенты определяют, **как эксперт думает, как работает и что выдаёт**. Например, [Security Engineer](engineering/engineering-security-engineer.md) проверяет код по OWASP Top 10 пункт за пунктом; [Frontend Developer](engineering/engineering-frontend-developer.md) рефакторит React-компоненты с учётом ARIA / доступности / performance budget.

---

## Быстрый старт

### Способ 1: установка одной командой

Поддержка **17 основных AI-инструментов** для разработки:

```bash
# Автодетект установленных инструментов и установка
./scripts/install.sh

# Или указать конкретный инструмент
./scripts/install.sh --tool openclaw       # OpenClaw ⭐ рекомендовано
./scripts/install.sh --tool claude-code    # Claude Code
./scripts/install.sh --tool copilot        # GitHub Copilot
./scripts/install.sh --tool cursor         # Cursor
./scripts/install.sh --tool kiro           # Kiro (Amazon)
./scripts/install.sh --tool trae           # Trae
./scripts/install.sh --tool opencode       # OpenCode
./scripts/install.sh --tool aider          # Aider
./scripts/install.sh --tool windsurf       # Windsurf
./scripts/install.sh --tool antigravity    # Antigravity
./scripts/install.sh --tool gemini-cli     # Gemini CLI
./scripts/install.sh --tool qwen           # Qwen Code
./scripts/install.sh --tool codex          # Codex CLI
./scripts/install.sh --tool deerflow       # DeerFlow 2.0 (ByteDance)
./scripts/install.sh --tool workbuddy      # WorkBuddy (Tencent)
./scripts/install.sh --tool hermes         # Hermes Agent (NousResearch)
./scripts/install.sh --tool qoder          # Qoder
```

> Claude Code и GitHub Copilot работают напрямую; остальным нужен `./scripts/convert.sh` для конвертации.

### Способ 2: ручное копирование

```bash
cp -r engineering/*.md ~/.claude/agents/

# Активация в Claude Code:
# "Активируй роль Frontend Developer и помоги собрать React-компонент"
```

### Способ 3: как референс промпта

Загляните в [CATALOG.md](CATALOG.md), скопируйте/адаптируйте под себя.

---

## Состав агентов

Полный каталог 187 агентов: **[CATALOG.md](CATALOG.md)**. Сводка по отделам:

| Отдел | Агентов | Типовые роли |
|-------|---------|--------------|
| 🛠️ Инжиниринг | 29 | Frontend, Backend Architect, AI Engineer, DevOps, Security, SRE, Embedded, FPGA |
| 🎨 Дизайн | 8 | UI/UX, Brand Guardian, Image Prompt Engineer, Visual Storyteller |
| 📢 Маркетинг | 30 | Growth Hacker, Content Creator, SEO, TikTok / Twitter / Instagram |
| 💰 Платный трафик | 7 | Аудит, Creative Strategist, PPC, Programmatic |
| 💼 Продажи | 8 | Account Strategist, Sales Coach, MEDDPICC, Outbound |
| 🏦 Финансы | 5 | Bookkeeper Controller, FP&A, Investment Researcher, Fraud Detection |
| 📦 Продукт | 5 | PM, Feedback Synthesizer, Trend Researcher |
| 📋 Проекты | 6 | Studio Producer, Experiment Tracker, Project Shipper |
| 🧪 Тестирование | 8 | Test Automation, API Tester, Performance Benchmarker |
| 🤝 Поддержка | 6 | Incident Communicator, Customer Insights Extractor |
| 🔬 Спец. области | 41 | Blockchain Security, SOC 2 / ISO 27001 / HIPAA Compliance, Legal Review, Real Estate, HR Onboarding |
| 🥽 Spatial Computing | 6 | XR User Research, AR/VR Engineer, Haptic Designer |
| 🎮 Game Dev | 20 | Unity Architect, Unreal, Godot, Roblox, Blender |
| 📖 Академические | 5 | Антрополог, Психолог, Историк, Нарратолог, Географ |

---

## 🇷🇺 Агенты для российского рынка — PRs Welcome

Перевод 184 апстрим-агентов завершён. Приветствуются PR для специфичных для РФ агентов:

- **Платформы РФ**: VK (ВКонтакте), Telegram bot operator, Yandex.Дзен, Rutube
- **E-commerce**: Wildberries seller, Ozon, Яндекс.Маркет, Авито продавец
- **Финтех**: Тинькофф-style product manager, СБП интеграция, Сбер API
- **SEO/Маркетинг**: Yandex SEO, ВК Реклама, MyTarget, Habr контент-стратегия
- **Compliance**: ФЗ-152 (Закон о персональных данных), ФЗ-149, КИИ, ФЗ-187
- **Корпоративные**: 1С интеграция, СБИС, ВКС (видеоконференции российские)

См. [CONTRIBUTING.md](CONTRIBUTING.md).

---

## Сценарии использования

### Сценарий 1: MVP для международного запуска

**Ваша команда**:
1. **Frontend Developer** — собирает React-приложение
2. **Backend Architect** — проектирует API и БД
3. **Growth Hacker** — планирует привлечение пользователей
4. **Rapid Prototyper** — быстрые итерации
5. **Reality Checker** — quality gate перед запуском

### Сценарий 2: Аудит безопасности + соответствия

**Ваша команда**:
1. **Security Engineer** — проверка кода по OWASP Top 10
2. **Blockchain Security Auditor** (если применимо) — анализ уязвимостей смарт-контрактов
3. **Compliance Auditor** — проверка SOC 2 / ISO 27001 / HIPAA
4. **Incident Communicator** — донесение рисков до руководства
5. **Technical Writer** — оформление отчёта аудита

---

## Вклад

Переводы, улучшения контента, новые агенты для российского рынка — всё welcome. Подробности в [CONTRIBUTING.md](CONTRIBUTING.md).

---

## Родственные проекты

| Проект | Позиционирование | Резюме |
|--------|------------------|--------|
| **Этот проект** (agency-agents-ru) | 🎭 Русскоязычная библиотека персон | 187 готовых к использованию AI-эксперта, PR для рынка РФ welcome |
| [agency-agents-zh](https://github.com/jnMetaCode/agency-agents-zh) ![](https://img.shields.io/github/stars/jnMetaCode/agency-agents-zh?style=flat&label=⭐) | 🇨🇳 Китайская версия | 215 агентов (165 переводов + 50 оригиналов под Китай — Xiaohongshu / Douyin / WeChat / Bilibili) |
| [agency-agents-ko](https://github.com/jnMetaCode/agency-agents-ko) | 🇰🇷 Корейская версия | 187 переведённых агента |
| [agency-agents-pt-BR](https://github.com/jnMetaCode/agency-agents-pt-BR) | 🇧🇷 Бразильская версия | 187 переведённых агента |
| [agency-agents](https://github.com/msitarzewski/agency-agents) | 🌏 Английский upstream | 184 оригинальных агента — основа этого проекта |
| [agency-orchestrator](https://github.com/jnMetaCode/agency-orchestrator) | 🚀 Движок оркестрации | Одна фраза → 187 эксперта сотрудничают, **результат за минуты** (9 LLM / 6 бесплатных) |

---

## Благодарности

- Английский оригинал: [msitarzewski/agency-agents](https://github.com/msitarzewski/agency-agents) (MIT)
- Спасибо автору [@msitarzewski](https://github.com/msitarzewski) за этот великолепный проект
- Русский перевод выполнен пакетно с помощью Claude Sonnet с ручной выверкой репрезентативных файлов. PR на улучшение стиля всегда welcome.

---

## Лицензия

MIT License — свободное использование, коммерческое или личное.

---

<div align="center">

**187 AI-агента, 17 инструментов, plug-and-play**

[⭐ Поставить звезду](https://github.com/jnMetaCode/agency-agents-ru) · [Открыть Issue](https://github.com/jnMetaCode/agency-agents-ru/issues) · [Внести вклад](https://github.com/jnMetaCode/agency-agents-ru/pulls)

На основе [agency-agents](https://github.com/msitarzewski/agency-agents), переведено и локализовано для русскоязычной аудитории

</div>
