# Eliza 🤖

<div align="center">
  <img src="/docs/static/img/eliza_banner.jpg" alt="Eliza Banner" width="100%" />
</div>

<div align="center">

📖 [Документація](https://elizaos.github.io/eliza/) | 🎯 [Приклади](https://github.com/thejoven/awesome-eliza)

</div>

## ✨ Особливості

- 🛠 Повноцінні коннектори для Discord, Twitter та Telegram
- 👥 Підтримка кількох агентів та кімнат
- 📚 Просте додавання та взаємодія з вашими документами
- 💾 Запам'ятовування контексту та зберігання документів
- 🚀 Висока масштабованість - створюйте свої власні дії та клієнти для розширення можливостей
- ☁️ Підтримує багато моделей, включаючи локальні Llama, OpenAI, Anthropic, Groq та інші
- 📦 Простота у використанні!

## 🎯 Для чого це можна використовувати?

- 🤖 Чат-боти
- 🕵️ Автономні агенти
- 📈 Обробка бізнес-процесів
- 🎮 NPC у відеоіграх
- 🧠 Торгівля

## 🌍 Переклади

<details>
<summary>Доступні мови</summary>

- [中文说明](./README_CN.md)
- [日本語の説明](./README_JA.md)
- [한국어 설명](./README_KOR.md)
- [Instructions en français](./README_FR.md)
- [Instruções em português](./README_PTBR.md)
- [Інструкція російською](./README_RU.md)

</details><br>

# 🚀 Початок роботи

**Необхідні умови (ОБОВ'ЯЗКОВО):**

- [Python 2.7+](https://www.python.org/downloads/)
- [Node.js 23.3+](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm)
- [pnpm](https://pnpm.io/installation)
    > **Для користувачів Windows:** потрібен WSL

### Редагування файлу .env

- Скопіюйте `.env.example` в `.env` та заповніть відповідними значеннями

```bash
cp .env.example .env
```

### Редагування файлу персонажа

1. Відкрийте `packages/core/src/defaultCharacter.ts`, щоб змінити персонажа за замовчуванням.

2. Для завантаження користувацьких персонажів:
    - Використовуйте команду `pnpm start --characters="path/to/your/character.json"`
    - Можна завантажувати кілька файлів персонажів одночасно.

### Запуск Eliza

Після налаштування файлу `.env` та файлу персонажа ви можете запустити бота за допомогою наступної команди:

```bash
pnpm i
pnpm build
pnpm start

# Проект швидко розвивається, іноді потрібно очищати проект, якщо ви повертаєтесь до нього через деякий час
pnpm clean
```

#### Додаткові вимоги

Можливо, буде потрібно встановити Sharp. Якщо при запуску виникне помилка, спробуйте встановити його за допомогою наступної команди:

```bash
pnpm install --include=optional sharp
```

# Налаштування середовища

Вам потрібно додати змінні середовища у файл `.env` для підключення до різних платформ:

```
# Обов'язкові змінні середовища
DISCORD_APPLICATION_ID=
DISCORD_API_TOKEN= # Токен бота
OPENAI_API_KEY=sk-* # API-ключ OpenAI, що починається з sk-
ELEVENLABS_XI_API_KEY= # API-ключ від elevenlabs
GOOGLE_GENERATIVE_AI_API_KEY= # API-ключ Gemini

# НАЛАШТУВАННЯ ELEVENLABS
ELEVENLABS_MODEL_ID=eleven_multilingual_v2
ELEVENLABS_VOICE_ID=21m00Tcm4TlvDq8ikWAM
ELEVENLABS_VOICE_STABILITY=0.5
ELEVENLABS_VOICE_SIMILARITY_BOOST=0.9
ELEVENLABS_VOICE_STYLE=0.66
ELEVENLABS_VOICE_USE_SPEAKER_BOOST=false
ELEVENLABS_OPTIMIZE_STREAMING_LATENCY=4
ELEVENLABS_OUTPUT_FORMAT=pcm_16000

TWITTER_DRY_RUN=false
TWITTER_USERNAME= # Ім'я користувача акаунта
TWITTER_PASSWORD= # Пароль акаунта
TWITTER_EMAIL= # Email акаунта

XAI_API_KEY=
XAI_MODEL=


# Для запитів до Claude
ANTHROPIC_API_KEY=

# EVM
EVM_PRIVATE_KEY=EXAMPLE_WALLET_PRIVATE_KEY

# Solana
SOLANA_PRIVATE_KEY=EXAMPLE_WALLET_PRIVATE_KEY
SOLANA_PUBLIC_KEY=EXAMPLE_WALLET_PUBLIC_KEY

# Fallback Wallet Configuration (deprecated)
WALLET_PRIVATE_KEY=EXAMPLE_WALLET_PRIVATE_KEY
WALLET_PUBLIC_KEY=EXAMPLE_WALLET_PUBLIC_KEY

BIRDEYE_API_KEY= # API-ключ для BirdEye

SOL_ADDRESS=So11111111111111111111111111111111111111112
SLIPPAGE=1
SOLANA_RPC_URL=https://api.mainnet-beta.solana.com
HELIUS_API_KEY= # API-ключ Helius


## Telegram
TELEGRAM_BOT_TOKEN= # Токен бота Telegram

TOGETHER_API_KEY=

```

# Локальне налаштування середовища

### Налаштування CUDA

Якщо у вас є NVIDIA GPU, ви можете встановити CUDA для значного прискорення локального інференсу.

```bash
pnpm install
npx --no node-llama-cpp source download --gpu cuda
```

Переконайтеся, що ви встановили CUDA Toolkit, включаючи cuDNN та cuBLAS.

### Локальний запуск

Додайте `XAI_MODEL` та встановіть його в одне з вищезгаданих значень з Запуску з Llama. Ви можете залишити `XAI_API_KEY` порожнім — модель буде завантажена з huggingface та оброблена локально.

# Клієнти

## Бот для Discord

Для отримання допомоги по налаштуванню бота Discord ознайомтесь з інструкцією: [Налаштування додатку бота](https://discordjs.guide/preparations/setting-up-a-bot-application.html).

### Спільнота та контакти

- [GitHub Issues](https://github.com/elizaos/eliza/issues). Найкраще підходить для: повідомлень про помилки при використанні Eliza та пропозицій нових функцій.
- [Discord](https://discord.gg/ai16z). Найкраще підходить для: обміну своїми додатками та спілкування з спільнотою.

## Контриб'ютори

<a href="https://github.com/elizaos/eliza/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=elizaos/eliza" />
</a>

## Історія зірок

[![Графік історії зірок](https://api.star-history.com/svg?repos=elizaos/eliza&type=Date)](https://star-history.com/#elizaos/eliza&Date)
