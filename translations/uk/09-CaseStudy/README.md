<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "6940b1e931e51821b219aa9dcfe8c4ee",
  "translation_date": "2025-06-23T11:21:20+00:00",
  "source_file": "09-CaseStudy/README.md",
  "language_code": "uk"
}
-->
# MCP у дії: реальні кейси

Model Context Protocol (MCP) змінює спосіб взаємодії AI-додатків із даними, інструментами та сервісами. У цьому розділі наведені реальні приклади, які демонструють практичне застосування MCP у різних корпоративних сценаріях.

## Огляд

Тут представлені конкретні приклади впровадження MCP, що показують, як організації використовують цей протокол для вирішення складних бізнес-завдань. Аналізуючи ці кейси, ви отримаєте уявлення про гнучкість, масштабованість і практичні переваги MCP у реальних умовах.

## Основні навчальні цілі

Вивчаючи ці кейси, ви:

- Зрозумієте, як MCP застосовується для розв’язання конкретних бізнес-проблем
- Ознайомитесь із різними патернами інтеграції та архітектурними підходами
- Визначите найкращі практики впровадження MCP у корпоративних середовищах
- Отримаєте уявлення про виклики та рішення, з якими стикаються у реальних проектах
- Виявите можливості застосування подібних підходів у власних проєктах

## Вибрані кейси

### 1. [Azure AI Travel Agents – Reference Implementation](./travelagentsample.md)

У цьому кейсі розглядається комплексне еталонне рішення Microsoft, яке демонструє, як створити багатоагентський AI-додаток для планування подорожей за допомогою MCP, Azure OpenAI та Azure AI Search. Проєкт включає:

- Оркестрацію багатьох агентів через MCP
- Інтеграцію корпоративних даних з Azure AI Search
- Безпечну та масштабовану архітектуру на базі Azure-сервісів
- Розширювані інструменти з повторно використовуваними компонентами MCP
- Конверсійний користувацький досвід на основі Azure OpenAI

Архітектура та деталі реалізації надають цінні знання про створення складних багатоагентських систем з MCP як координаційним шаром.

### 2. [Оновлення елементів Azure DevOps на основі даних YouTube](./UpdateADOItemsFromYT.md)

Цей кейс демонструє практичне застосування MCP для автоматизації робочих процесів. Показано, як MCP-інструменти допомагають:

- Витягувати дані з онлайн-платформ (YouTube)
- Оновлювати робочі елементи в Azure DevOps
- Створювати повторювані автоматизовані процеси
- Інтегрувати дані між різними системами

Цей приклад ілюструє, що навіть відносно прості впровадження MCP можуть суттєво підвищити ефективність, автоматизуючи рутинні завдання та покращуючи узгодженість даних.

### 3. [Отримання документації в реальному часі з MCP](./docs-mcp/README.md)

У цьому кейсі ви навчитеся підключати консольний клієнт на Python до MCP-сервера для отримання та запису актуальної, контекстно-залежної документації Microsoft у реальному часі. Ви дізнаєтеся, як:

- Підключатися до MCP-сервера через Python-клієнт та офіційний MCP SDK
- Використовувати потокові HTTP-клієнти для ефективного отримання даних у реальному часі
- Викликати інструменти документації на сервері та виводити відповіді безпосередньо в консоль
- Інтегрувати актуальну документацію Microsoft у робочий процес без виходу з терміналу

Розділ містить практичне завдання, мінімальний робочий код та посилання на додаткові ресурси для поглибленого вивчення. Перегляньте повний покроковий опис і код у посиланні, щоб зрозуміти, як MCP може змінити доступ до документації та підвищити продуктивність розробників у консольних середовищах.

### 4. [Інтерактивний веб-додаток для генерації плану навчання з MCP](./docs-mcp/README.md)

Цей кейс показує, як створити інтерактивний веб-додаток за допомогою Chainlit та MCP для генерації персоналізованих планів навчання з будь-якої теми. Користувачі можуть вказати предмет (наприклад, «сертифікація AI-900») та тривалість навчання (наприклад, 8 тижнів), а додаток надасть покроковий тижневий розклад рекомендованого контенту. Chainlit забезпечує розмовний чат-інтерфейс, роблячи процес захопливим і адаптивним.

- Розмовний веб-додаток на базі Chainlit
- Користувацькі запити для вибору теми та тривалості
- Тижневі рекомендації контенту за допомогою MCP
- Реактивні, адаптивні відповіді у чат-інтерфейсі

Проєкт демонструє, як поєднати conversational AI та MCP для створення динамічних освітніх інструментів із орієнтацією на користувача у сучасному веб-середовищі.

### 5. [Документація в редакторі з MCP-сервером у VS Code](./docs-mcp/README.md)

Цей кейс показує, як інтегрувати Microsoft Learn Docs безпосередньо у VS Code за допомогою MCP-сервера — більше не потрібно перемикатися між вкладками браузера! Ви дізнаєтеся, як:

- Швидко шукати та читати документацію прямо у VS Code через панель MCP або командну палітру
- Посилатися на документацію та вставляти посилання безпосередньо у README або markdown-файли курсів
- Використовувати GitHub Copilot разом з MCP для безперебійної роботи з документацією та кодом на основі AI
- Перевіряти та покращувати документацію за допомогою зворотного зв’язку в реальному часі та достовірності від Microsoft
- Інтегрувати MCP з GitHub workflow для безперервної перевірки документації

Реалізація включає:
- Приклад `.vscode/mcp.json` конфігурації для швидкого налаштування
- Покрокові інструкції з використання інтерфейсу редактора на основі скріншотів
- Поради щодо поєднання Copilot і MCP для максимальної продуктивності

Цей сценарій ідеально підходить для авторів курсів, технічних письменників та розробників, які хочуть залишатися зосередженими в редакторі, працюючи з документацією, Copilot та інструментами перевірки — усе це на базі MCP.

### 6. [Створення MCP-сервера з APIM](./apimsample.md)

У цьому кейсі наведено покрокову інструкцію зі створення MCP-сервера за допомогою Azure API Management (APIM). Розглядаються:

- Налаштування MCP-сервера в Azure API Management
- Експонування API-операцій як MCP-інструментів
- Конфігурація політик для обмеження частоти запитів і безпеки
- Тестування MCP-сервера з використанням Visual Studio Code та GitHub Copilot

Цей приклад ілюструє, як використовувати можливості Azure для створення надійного MCP-сервера, який можна застосовувати в різних додатках, покращуючи інтеграцію AI-систем із корпоративними API.

## Висновок

Ці кейси підкреслюють гнучкість і практичне застосування Model Context Protocol у реальних умовах. Від складних багатоагентських систем до цільових автоматизованих процесів — MCP забезпечує стандартизований спосіб поєднання AI-систем із необхідними інструментами та даними для створення цінності.

Вивчаючи ці реалізації, ви отримаєте знання про архітектурні патерни, стратегії впровадження та найкращі практики, які можна застосувати у власних проєктах MCP. Приклади доводять, що MCP — це не просто теоретична концепція, а практичне рішення для реальних бізнес-завдань.

## Додаткові ресурси

- [Azure AI Travel Agents GitHub Repository](https://github.com/Azure-Samples/azure-ai-travel-agents)
- [Azure DevOps MCP Tool](https://github.com/microsoft/azure-devops-mcp)
- [Playwright MCP Tool](https://github.com/microsoft/playwright-mcp)
- [Microsoft Docs MCP Server](https://github.com/MicrosoftDocs/mcp)
- [MCP Community Examples](https://github.com/microsoft/mcp)

**Відмова від відповідальності**:  
Цей документ було перекладено за допомогою сервісу автоматичного перекладу [Co-op Translator](https://github.com/Azure/co-op-translator). Хоча ми прагнемо до точності, просимо враховувати, що автоматичні переклади можуть містити помилки або неточності. Оригінальний документ рідною мовою слід вважати авторитетним джерелом. Для критично важливої інформації рекомендується звертатися до професійного людського перекладу. Ми не несемо відповідальності за будь-які непорозуміння або неправильні тлумачення, що виникли внаслідок використання цього перекладу.