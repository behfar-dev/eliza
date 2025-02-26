# Eliza 🤖

<div align="center">
  <img src="./docs/static/img/eliza_banner.jpg" alt="Eliza Banner" width="100%" />
</div>

<div align="center">

📖 [Dokumentáció](https://elizaos.github.io/eliza/) | 🎯 [Példák](https://github.com/thejoven/awesome-eliza)

</div>

## ✨ Funkciók

- 🛠️ Teljes funkcionalitású Discord, Twitter és Telegram összekötők
- 🔗 Támogatás minden modellhez (Llama, Grok, OpenAI, Anthropic, etc.)
- 👥 Többügynök és szobatámogatás
- 📚 Könnyen feldolgozhatja és kezelheti dokumentumait
- 💾 Helyrehozható memória és dokumentumtár
- 🚀 Magas fokú bővíthetőség - hozz létre saját műveleteket és klienseket
- ☁️ Számos modell támogatása (helyi Llama, OpenAI, Anthropic, Groq stb.)
- 📦 Egyszerűen működik!

## 🎯 Felhasználási területek

- 🤖 Chatbotok
- 🕵️ Autonóm ügynökök
- 📈 Üzleti folyamatkezelés
- 🎮 Videójáték NPC-k
- 🧠 Kereskedés

## 🚀 Gyors kezdés

### Előfeltételek

- [Python 2.7+](https://www.python.org/downloads/)
- [Node.js 23+](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm)
- [bun](https://bun.io/installation)

> **Megjegyzés Windows-felhasználóknak:** [WSL 2](https://learn.microsoft.com/en-us/windows/wsl/install-manual) szükséges.

### Használja az Indítót (Ajánlott)

```bash
git clone https://github.com/elizaos/eliza-starter.git
cd eliza-starter
cp .env.example .env
bun i && bun run build && bun start
```

Miután az ügynök elindult, a folyamat végén egy üzenetet kell látnod, amely arra utal, hogy futtasd a "bun start:client" parancsot.
Nyiss egy másik terminált, navigálj ugyanabba a könyvtárba, és futtasd az alábbi parancsot, majd kövesd az URL-t, hogy kommunikálhass az ügynököddel:

```bash
bun start:client
```

Ezután olvasd el a [Dokumentációt](https://elizaos.github.io/eliza/) hogy megtanuld, hogyan testreszabhatod Elizát.

### Eliza manuális indítása (Csak akkor ajánlott, ha pontosan tudod, mit csinálsz)

```bash
# Klónozd a repót
git clone https://github.com/elizaos/eliza.git

# Válts a legfrissebb kiadásra
# A projekt gyorsan fejlődik, ezért ajánlott a legfrissebb kiadásra váltani
git checkout $(git describe --tags --abbrev=0)
```

### Szerkezd a .env fájlt

Másold a .env.example fájlt .env néven, és töltsd ki a megfelelő értékekkel.

```
cp .env.example .env
```

Megjegyzés: A .env fájl opcionális. Ha több különálló ügynököt szeretnél futtatni, a titkos adatokat a karakter JSON-on keresztül is megadhatod.

### Eliza automatikus indítása

Ez a parancs mindent beállít a projekthez, és elindítja a botot az alapértelmezett karakterrel.

```bash
sh scripts/start.sh
```

### Karakterfájl szerkesztése

``

1. Nyisd meg a `packages/core/src/defaultCharacter.ts` fájlt, hogy módosítsd az alapértelmezett karaktert. Kommentezd ki és szerkeszd.

2. Egyedi karakterek betöltése:
    - Használhatod a következőt: `bun start --characters="path/to/your/character.json"`
    - Több karakterfájl is betölthető egyszerre.
3. Kapcsolódás X-hez (Twitter)
    - Módosítsd a `"clients": []` részt `"clients": ["twitter"]` -re a karakterfájlban, hogy csatlakozz az X-hez

### Eliza manuális indítása

```bash
bun i
bun run build
bun start
```

#### További követelmények

Előfordulhat, hogy telepítened kell a Sharpot. Ha hibát látsz az indításkor, próbáld meg telepíteni az alábbi paranccsal:

```
bun install --include=optional sharp
```

### Közösség és kapcsolattartás

- [GitHub Issues](https://github.com/elizaos/eliza/issues). Ideális hibák jelentésére és új funkciók javaslatára.
- [Discord](https://discord.gg/ai16z). BTökéletes hely az alkalmazásaid megosztására és a közösséggel való kapcsolatépítésre.

## Közreműködők

<a href="https://github.com/elizaos/eliza/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=elizaos/eliza" />
</a>

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=elizaos/eliza&type=Date)](https://star-history.com/#elizaos/eliza&Date)
