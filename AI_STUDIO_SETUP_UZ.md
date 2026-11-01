# Google AI Studio'da Web Design Agent'ni o'rnatish

## Tavsiya etilgan yo'l: Playground → Agents

Google AI Studio hozir ikkita alohida ish rejimini taklif qiladi. **Playground → Agents** maxsus agentning persona, skills va knowledge fayllarini sozlash uchun mos. **Build mode** esa keyinroq haqiqiy web-ilovani yaratish, kodini tahrirlash va preview/deploy qilish uchun ishlatiladi.

### 1. Paketni tayyorlash
1. ZIP arxivni kompyuteringizga yuklab oling.
2. Arxivni oching.
3. Ichidagi `.agents/` papkasini saqlang. Bu papkadagi `AGENTS.md` va `skills/*/SKILL.md` agentning asosiy xulqi va ko'nikmalaridir.
4. `knowledge/`, `templates/` va `prompts/` papkalarini ham saqlang.

### 2. Agent Playground'ni ochish
1. https://aistudio.google.com/ saytiga kiring.
2. Chap menyudan **Playground** bo'limini oching.
3. Playground ichida **Agents** rejimiga o'ting.
4. Agent shablonini tanlang yoki mavjud bo'lsa bo'sh/bazaviy agentdan boshlang.

### 3. Kerakli tool'larni yoqish
Agent settings ichida quyidagilarni yoqing:
- **Google Search** — zamonaviy dizayn referenslari, rasmiy qo'llanmalar va raqobatchilarni izlash.
- **URL Context** — foydalanuvchi bergan sayt URL'larini o'qish va tahlil qilish.
- **Code Execution** — Bash/Python orqali fayllar, kod va test buyruqlari bilan ishlash.
- **Filesystem Tools** — loyiha va knowledge fayllarini o'qish/yozish.

Bu agent uchun dastlab boshqa tashqi MCP yoki maxsus API ulash shart emas.

### 4. Fayllarni environment'ga ulash
Environment panelida **Add Sources** tugmasini bosing. Hozirgi hujjatlardagi manba turlari: Inline Files, Google Cloud Storage va GitHub repository.

**Eng sodda usul — Inline Files:** fayllarni kerakli destination path bilan alohida qo'shing. Minimal majburiy fayllar:
- `.agents/AGENTS.md`
- Har bir `.agents/skills/<skill-name>/SKILL.md`

Knowledge fayllarini ham `knowledge/...` yo'llariga qo'shing. Agentga fayllarni kerak bo'lganda o'qishni ayting. `templates/` va `prompts/` ham shu yo'l bilan qo'shilishi mumkin.

**Versiya nazorati uchun — GitHub:** paketni o'zingizning GitHub repository'ingizga joylab, Environment → Add Sources → GitHub Repository orqali ulang. Private repository uchun faqat zarur ruxsatga ega token ishlating. Repozitoriy root'ida `.agents/` papkasi bo'lishi kerak; Sources panelida mount path va agent environment root'ini tekshiring.

Muhim: birinchi agent xabarini yuborganingizdan keyin joriy session environment sozlamalarini o'zgartirib bo'lmaydi. Barcha fayl va tool'larni avval ulang.

### 5. Agentni ishga tushirish testi
Birinchi xabar sifatida quyidagini yuboring:

> Read `.agents/AGENTS.md`, list all discovered skills, and inspect the `knowledge/` directory. Do not modify any project files. Return a concise capability map and tell me which skill you would use for: (1) auditing an existing website, (2) redesigning a dashboard, and (3) implementing a responsive React page. Do not claim files are loaded unless you can actually read them.

To'g'ri ishlasa, agent o'z rolini tushuntirib, skill fayllarini topishi va ularning vazifasini aytishi kerak.

### 6. Kundalik foydalanish

**Audit:** `prompts/01-audit-existing-site.md` matnini yuboring, URL yoki repository'ni almashtiring.

**Redesign konsepsiyasi:** `prompts/02-redesign-direction.md`.

**Kodga joriy qilish:** `prompts/03-implement-redesign.md`.

**Mobil va accessibility tekshiruvi:** `prompts/04-responsive-accessibility-pass.md`.

**Yakuniy polish:** `prompts/05-visual-polish.md`.

**Topshirish:** `prompts/06-handoff.md`.

Har bir topshiriqda aniq scope va stop condition bo'lsin. Masalan: "Faqat /dashboard sahifasini tekshir; kodga tegma; audit hisobotini yozgach to'xta."

### 7. AI Studio Build mode'da sayt yaratish
Agentning o'zi bilan audit va dizayn strategiyasini tayyorlaganingizdan so'ng:
1. AI Studio'da **Build** rejimini oching.
2. Mavjud loyihani `Add files → Import from GitHub` orqali olib kirish yoki yangi ilova yaratish mumkin.
3. Agent tayyorlagan audit, redesign direction va design tokens hujjatlarini Build promptiga biriktiring.
4. Kodni Preview va Code tab'larida tekshiring; kerak bo'lsa Annotation mode orqali elementni belgilab tuzatish so'rang.
5. GitHub sync yoki ZIP export bilan kodni alohida saqlang.
6. Faqat tayyor bo'lgach Cloud Run deploy qiling; deploy xarajatlarini oldindan tekshiring.

Build mode odatda React frontend va Node.js server runtime yaratadi. Firebase Authentication/Firestore va server-side secrets kabi imkoniyatlar mavjud bo'lishi mumkin, ammo agent har bir yangi loyihada ularni haqiqatan sozlanganini tekshirishi kerak.

### 8. Model tanlash
- Murakkab audit, arxitektura va kod yozish uchun UI'da mavjud eng kuchli reasoning/coding modelini tanlang.
- Tez iteratsiya va kichik CSS tuzatishlari uchun tezroq model yetarli bo'lishi mumkin.
- Model nomlari va mavjudligi o'zgaradi; qat'iy model nomiga bog'lanib qolmang.

### 9. Xarajat va xavfsizlik
- Managed agent mustaqil rejalashtirishi, kod bajarishi va qayta urinishi mumkin; keraksiz uzoq vazifalar token va API xarajatini oshiradi.
- Har bir promptga scope va yakunlash shartini yozing.
- Network allowlist'ga faqat kerakli domenlarni kiriting; keng wildcard'lardan qoching.
- API token, production credentials yoki to'liq admin ruxsatlarini agentga bermang.
- Production deploy, Git push, ma'lumot o'chirish va xavfli migratsiyalar faqat sizning aniq topshirig'ingiz bilan bajarilsin.
- Agent chiqargan kodni test qiling; avtomatik tekshiruvlar inson ko'rigini to'liq almashtirmaydi.

### 10. Muhim farq
Agar siz oddiy Chat prompt/Run settings rejimidan foydalansangiz, `.agents/AGENTS.md` va skill'lar avtomatik yuklanmaydi. Bunday holatda System Instructions maydoniga `.agents/AGENTS.md` matnini qo'lda joylashtiring va zarur skill matnlarini kerakli topshiriqqa qo'shing. To'liq skills workflow uchun **Playground → Agents** rejimidan foydalaning.

## Rasmiy hujjatlar
- Agents in AI Studio Playground: https://ai.google.dev/gemini-api/docs/aistudio-agents
- Building managed agents: https://ai.google.dev/gemini-api/docs/custom-agents
- Build apps in AI Studio: https://ai.google.dev/gemini-api/docs/aistudio-build-mode
- WCAG 2.2: https://www.w3.org/TR/WCAG22/
- Core Web Vitals: https://developers.google.com/search/docs/appearance/core-web-vitals
