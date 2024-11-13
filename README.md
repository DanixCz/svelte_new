# K čemu je Svelte.kit 5?
Svelte.kit je moderní frontendový framework zaměřený na jednoduchost a efektivitu. Na rozdíl od jiných frameworků, jako je React nebo Vue, se Svelte liší tím, že nepracuje jako běhová knihovna, která je načtena v prohlížeči. Místo toho Svelte během kompilace přeloží váš kód do čistého, optimalizovaného JavaScriptu, což znamená, že aplikace nepotřebuje těžký runtime a má nižší režii. To zajišťuje rychlejší načítání stránek a lepší výkon aplikací.

SvelteKit je framework postavený na Svelte, který umožňuje snadnou tvorbu plnohodnotných webových aplikací. Kromě práce s komponentami, jako je tomu v Svelte, SvelteKit poskytuje vestavěné routování, server-side rendering (SSR) a mnoho dalších nástrojů pro vývoj moderních aplikací.

# Důležité odkazy pro Svelte.kit 5

- [Oficiální dokumentace SvelteKit](https://kit.svelte.dev/docs) – Podrobná dokumentace k SvelteKit, která obsahuje vše od základních konceptů po pokročilá témata.
- [SvelteKit Demo](https://kit.svelte.dev/examples) – Ukázkové projekty ve SvelteKit, které vám pomohou lépe pochopit, jak SvelteKit funguje v praxi.
- [Svelte REPL](https://svelte.dev/repl) – Online nástroj pro experimentování se Svelte a SvelteKit kódem přímo v prohlížeči.
- [SvelteKit GitHub](https://github.com/sveltejs/kit) – Repozitář na GitHubu, kde můžete sledovat vývoj SvelteKit a přispívat do projektu.
- [SvelteKit 5 rozdíly od SvelteKit 4](https://sveltekit.io/blog/svelte-5) – Zde najdete některé základní změny ve SvelteKit 5, která by měla být vydaná jako officiální verze.


# Instalace a popis SvelteKit 5

Tento návod popisuje, jak nainstalovat SvelteKit 5 a vytvořit čistý projekt.

## 1. Instalace

Nejdříve je třeba mít nainstalovaný [Node.js](https://nodejs.org/), doporučuje se verze 16 nebo vyšší. Dále postupujte podle následujících kroků:

### Instalace svelte

Instalaci provádíme pomocí příkazu v terminalu.

Máte na výběr ze dvouch způsobu:

#### 1. Možnost: Pokud chceme mít svelte přímo ve složce, která bude pojmenovaná.

```bash
npm create svelte@latest my-sveltekit-app
```
Poté se do složky přesuneme.

```bash
cd my-sveltekit-app
```

#### 2. Možnost: Pro snadnou instalaci přímo ve složce (doporučujeme).

```bash
npm install svelte@latest
```

Jako první se nás terminál zeptá:

```bash
Need to install the following packages:
create-svelte@6.3.10
Ok to proceed? (y)
```

Zde se nás svelte ptá, zda chceme nainstalovat nejnovejší verzi svelte, odpovíte "y", jak tomu je napsáno v konzoli. Pro zrušení stačí zmáčknout "ENTER".
Dále se Vás svelte zeptá, kam chcete projekt nainstalovat.
Pokud jste ve složce, ve kterém chcete mít svelte.kit, potvrdíme klávesovou zkratkou "ENTER".

```bash
create-svelte version 6.3.10

┌  Welcome to SvelteKit!
│
◆  Where should we create your project?
│    (hit Enter to use current directory)
└
```

Zde Vás ještě svelte upozorní, že je složka prázdna a zda chcete pokračovat. Pomocí šipek zvolte "Yes"

```bash
◆  Directory not empty. Continue?
│  ● Yes / ○ No
└
```

Následně si vyberete verzi projektu:
- **SvelteKit demo app** – Slouží jako ukázka, jak se svelte má používat v testovacím projektu.
- **Skeleton project** – Ideální volba pro vytvoření čistého projektu pro tvorbu webové aplikace.
- **Library project** - Slouží pro vytváření knihovny komponent.

```bash
◆  Which Svelte app template?
│  ● SvelteKit demo app (A demo app showcasing some of the features of SvelteKit - play a word guessing game that works without JavaScript!)
│  ○ Skeleton project
│  ○ Library project
└
```

Zde si volíte typ projektu, jakou bude mít jazykovou logiku:

- **Yes, using TypeScript syntax** – Při této volbě bude projekt nastaven tak, aby používal **TypeScript** pro psaní kódu. TypeScript je nadmnožina JavaScriptu, která poskytuje statické typování a větší bezpečnost kódu.
- **Yes, using JavaScript with JSDoc comments** – Tento režim umožňuje používat běžný JavaScript, ale přidává možnost typové kontroly prostřednictvím **JSDoc komentářů**, které poskytují podobné výhody jako TypeScript, aniž byste museli psát v TypeScriptu.
- **No** – Tato volba vypne jakoukoliv typovou kontrolu, projekt bude nastaven čistě pro použití **JavaScriptu** bez TypeScriptu nebo JSDoc komentářů.

```bash
◆  Add type checking with TypeScript?
│  ● Yes, using TypeScript syntax
│  ○ Yes, using JavaScript with JSDoc comments
│  ○ No
└
```

Dále si již volíte logiku projektu, zde se volí klávesou "SPACE" a posouvate se šipkama na klávesnici.

Definicice jednotlivých voleb:
- **Add ESLint for code linting** – Přidá nástroj **ESLint**, který pomáhá automaticky kontrolovat a opravovat chyby ve stylu a syntaxi kódu, čímž zvyšuje jeho kvalitu a konzistenci.
- **Add Prettier for code formatting** – Přidá **Prettier**, který se postará o automatické formátování kódu podle předem definovaných pravidel, čímž zajistí jeho jednotný vzhled napříč celým projektem.
- **Add Playwright for browser testing** – Přidá nástroj **Playwright** pro provádění end-to-end testování v různých prohlížečích, což umožňuje testování webových aplikací za různých podmínek.
- **Add Vitest for unit testing** – Přidá **Vitest**, který slouží k psaní a spouštění jednotkových testů, což umožňuje testovat jednotlivé funkce nebo komponenty aplikace izolovaně.
- **Try the Svelte 5 preview (unstable!)** – Aktivuje možnost vyzkoušet nestabilní verzi **Svelte 5**, která může obsahovat nové funkce a experimentální vlastnosti, ale nemusí být ještě plně stabilní.

Osobně zde volíme první dvě a zatím i Svelte 5 preview.

```bash
◆  Select additional options (use arrow keys/space bar)
│  ◻ Add ESLint for code linting
│  ◻ Add Prettier for code formatting
│  ◻ Add Playwright for browser testing
│  ◻ Add Vitest for unit testing
│  ◻ Try the Svelte 5 preview (unstable!)
└
```

### Instalace projektu svelte

Pokud chceme mít svelte.kit nahraný přímo ve složce, ve které jsme.

```bash
npm create svelte@latest
```

### Instalace node modulu.

Bez tohoto modulu Vám nebude fungovat spuštení projektu. Pozor, node moduli se nepřesouvají do repozitáře, pokud budete na jiném PC, musíte tyto moduly znovu nainstalovat.

```bash
npm install
```

### Pro spuštění aplikace se změnama v realnem čase.

```bash
npm run dev
```

Pro ukončení stačí v terminálu dát klávesovou zkratku CTRL + C, nebo napsat "q" a potvrdit tlačítkem "ENTER".

## 2. Struktura projektu

Po vytvoření projektu uvidíte následující strukturu:

```lua
├── src/
│   ├── lib/
│   ├── routes/
│   │   ├── +page.svelte
│   │   ├── +layout.svelte
│   │   ├── +page.server.ts/js
│   │   ├── +error.svelte
│   │   ├── +server.ts/js
│   ├── app.d.ts
├── static/
├── svelte.config.js
├── tsconfig.json
├── vite.config.ts
├── package.json
└── .env
```

### Popis klíčových složek a souborů

#### `src/`
Základní složka, kde se nachází veškerý zdrojový kód aplikace.

- **`lib/`** – Sem patří sdílené komponenty a moduly, které budete používat na různých místech aplikace. Např. vlastní komponenty nebo utility.
- **`routes/`** – Obsahuje soubory a složky, které představují jednotlivé stránky vaší aplikace.

#### Důležité soubory v `routes/`:

- **`+page.svelte`** – Komponenta, která definuje obsah dané stránky.
- **`+layout.svelte`** – Komponenta, která slouží jako základní layout pro stránky. Může obsahovat navigaci, hlavičku a další prvky, které se opakují.
- **`+page.server.ts/js`** – Zpracovává server-side logiku specifickou pro danou stránku. Sem můžete např. zpracovávat formuláře nebo fetchovat data.
- **`+error.svelte`** – Komponenta, která se vykreslí při chybě (např. 404 nebo 500).
- **`+server.ts/js`** – Soubor pro server-side operace na úrovni dané trasy (např. API volání).

#### Ostatní klíčové soubory:

- **`.env`** – Soubor pro ukládání citlivých dat (API klíče, přihlašovací údaje). Tento soubor nesmí být nahrán do veřejného repozitáře. Vždy ho přidejte do `.gitignore`.
- **`svelte.config.js`** – Konfigurační soubor pro SvelteKit. Zde nastavíte adaptér (pro nasazení na různé platformy) a další volby jako cesty.
- **`tsconfig.json`** – Konfigurační soubor pro TypeScript. Pokud používáte TypeScript, zde můžete upravovat nastavení kompilátoru.
- **`vite.config.ts`** – Konfigurační soubor pro Vite.js, který SvelteKit používá pro bundlování kódu. Zde můžete přidávat pluginy a upravovat chování vývojového serveru.
- **`package.json`** – Obsahuje seznam závislostí projektu, skripty (např. `dev`, `build`) a další metadata o projektu.
- **`package-lock.json`** – Uzamkne verze závislostí, aby se zajistilo, že každý uživatel projektu bude používat stejné verze.

---

## 3. Základní syntaxe a soubory v SvelteKit

Zde jsou hlavní soubory, se kterými budete pracovat:

### **`+page.svelte`**
Tento soubor slouží k definování obsahu pro jednotlivé stránky. Obsahuje HTML, CSS a JavaScript/TypeScript.

Ukázkový příklad:

```svelte
<script>
  let name = "World";
</script>

<h1>Hello {name}!</h1>

<style>
  h1 {
    color: purple;
  }
</style>
```

### **`+page.server.ts/js`**
Tento soubor obsahuje server-side logiku spojenou s konkrétní stránkou, např. zpracování formulářů nebo načítání dat.

Ukázkový příklad (TypeScript):

```typescript
export const load = async ({ fetch }) => {
  const res = await fetch('/api/data');
  const data = await res.json();
  return { props: { data } };
};
```

### **`+layout.svelte`**
Tento soubor definuje strukturu stránek a sdílené komponenty, které se mají zobrazit na všech stránkách, např. navigaci nebo patičku. Složí jako šablona

```typescript
<nav>
  <a href="/">Home</a>
  <a href="/about">About</a>
</nav>

<slot></slot>
```

### **`+server.ts/js`**
Tento soubor slouží k zpracování HTTP požadavků na úrovni serveru. Můžete jej použít k vytvoření API koncových bodů.

```typescript
import type { RequestHandler } from '@sveltejs/kit';

export const GET: RequestHandler = async () => {
  return {
    status: 200,
    body: { message: 'Hello from the server!' }
  };
};
```

### **`+error.svelte`**
Soubor, který se zobrazuje při chybě (např. 404 nebo 500).

```typescript
<script>
  export let status;
  export let error;
</script>

<h1>{status}</h1>
<p>{error.message}</p>
```

### **`+error.svelte`**
Tento soubor se používá k zobrazení chybových stránek (např. 404 nebo 500). Zobrazuje status chyby a odpovídající zprávu.

Ukázkový příklad:

```svelte
<script>
  export let status;
  export let error;
</script>

<h1>{status}</h1>
<p>{error.message}</p>
```
## 4. Co patří do složky `lib/`

Složka `lib/` je určena pro sdílené moduly a komponenty, které chcete používat napříč celou aplikací. Typicky sem patří:

- **Vlastní UI komponenty** – například tlačítka, modální okna, hlavičky apod.
- **Utility funkce** – například funkce pro formátování dat, validaci formulářů, apod.
- **Sdílené CSS styly nebo proměnné** – globální styly, které se používají v celé aplikaci.

Doporučená struktura složky `lib/` může vypadat takto:
```lua
lib/
├── components/
│   ├── Button.svelte
│   └── Modal.svelte
├── utils/
│   └── formatDate.ts
└── styles/
    └── global.css
```

---

## 5. Význam klíčových konfiguračních souborů

- **`.env`** – Tento soubor slouží k ukládání citlivých informací, jako jsou API klíče nebo přihlašovací údaje. Je důležité, aby byl zahrnut do `.gitignore`, a tak nebyl nahráván do veřejných repozitářů.
  
- **`svelte.config.js`** – Konfigurační soubor pro SvelteKit. Zde můžete nastavovat různé parametry projektu, včetně adaptéru, který se používá pro nasazení aplikace. Můžete zde také upravovat různé volby, jako jsou cesty k souborům nebo nastavení CSS preprocessingu.

- **`tsconfig.json`** – Tento soubor určuje nastavení TypeScriptu, pokud používáte TypeScript. Obsahuje různé volby pro kompilaci, které mohou ovlivnit, jak TypeScript kontroluje váš kód a jak generuje výstupní JavaScript.

- **`vite.config.ts`** – Konfigurační soubor pro Vite.js, což je nástroj pro bundlování, který používá SvelteKit. Můžete zde definovat různé pluginy, optimalizace a nastavení chování během vývoje a produkce.

- **`package.json`** – Tento soubor obsahuje metadata o projektu, jako jsou název, verze a závislosti. Také obsahuje různé skripty, které můžete spouštět pro správu projektu, jako například `npm run dev` pro spuštění vývojového serveru.

- **`package-lock.json`** – Tento soubor uzamyká verze závislostí vašeho projektu. Zajišťuje, že každý, kdo instaluje projekt, bude mít stejné verze balíčků, což zajišťuje konzistenci mezi vývojovým a produkčním prostředím.

---

## 6. Spuštění projektu a další kroky

Pro spuštění projektu v režimu vývoje použijte následující příkaz:

```bash
npm run dev
```

Tímto se spustí lokální server, který bude automaticky reflektovat změny, které v projektu provedete.

Pro sestavení produkční verze projektu použijte:

```bash
npm run build
```

To vytvoří optimalizovanou verzi aplikace připravenou k nasazení.

Pro spuštění projektu v produkčním režimu po jeho sestavení použijte následující příkaz:

```bash
npm run preview
```
Tento příkaz spustí aplikaci ve stejném prostředí, ve kterém bude fungovat v produkci, takže si můžete otestovat, jak bude aplikace vypadat po nasazení.
---

Tento návod poskytuje kompletní přehled o instalaci, konfiguraci a spuštění SvelteKit 5 projektu. Po jeho dokončení budete mít k dispozici plně funkční aplikaci připravenou k dalšímu vývoji a nasazení do produkčního prostředí.
