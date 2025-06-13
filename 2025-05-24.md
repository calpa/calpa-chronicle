---
theme: dracula
title: 用 Bolt.new 實作 3 款手機 App：零程式也能 1 小時做出作品
transition: fade
mdc: true
---

<LoadingScene />

---
layout: center
class: bg-[#172966] text-white font-mono
---

<div class="text-3xl font-bold text-center leading-snug">
  用 Bolt.new + Expo<br />
  零程式也能 1 小時做出 3 款手機 App
</div>
<div class="text-xs opacity-50">2025-05-24</div>

<div class="text-xs italic opacity-50">Calpa Liu</div>

---
layout: center
class: bg-[#172966] text-white font-mono
---

<div class="text-xl opacity-70 mb-2">你是不是也曾經想過...</div>

<div class="text-2xl sm:text-3xl font-bold leading-snug text-red-400" v-click.hide>
  「我有一個 App 點子，<br />但完全不會寫程式該怎麼辦？」
</div>

<div class="text-2xl sm:text-3xl text-green-300 mt-6" v-after>
  今天，我會帶你用 Bolt.new + Expo，<br />
  在 1 小時內實作出 3 款真的能跑的手機 App！
</div>


---
layout: two-cols
class: flex flex-col h-full justify-center items-center gap-4
---

## 歡迎加入 Discord！

- 本場講座將在 Discord 上與大家互動
- 進入指定頻道可隨時發問
- 你也可以用 emoji 或貼圖來參與討論、表達想法

<div class="text-blue-400">https://discord.gg/Cb9F6MTC26</div>

::right::

![Discord QR Code](https://api.qrserver.com/v1/create-qr-code/?size=150x150&data=https://discord.gg/Cb9F6MTC26&bgcolor=172966&color=ffffff)

---
layout: two-cols
class: flex flex-col h-full justify-center items-center gap-4
---

## 👋 大家好，我是 Calpa

- 2017 年開始寫程式，一路從全端工程師走到 Web3 領域
- 2025 年開始每天分享技術文章，現在累積已超過 270 篇
- 我用 ChatGPT + Bolt.new 實作過 10+ 個 AI 工具 App
- 喜歡用簡單的方法解釋複雜的技術，也辦過 6 場 AI 實作分享會！

::right::

<img src="https://assets.calpa.me/public/pfp.avif" class="rounded-full w-36 h-36 border-4 border-white shadow-lg" alt="Calpa Liu">

<div class="text-xl font-bold mt-2">Calpa Liu</div>
<div class="text-sm opacity-70">全端工程師 / AI 工具愛好者 / 技術寫作者</div>


---
class: flex flex-col h-full justify-center items-center gap-4
---

<Events filter="before" />

---
layout: center
---

## 到底我用 AI 做了什麼？

---
layout: two-cols
class: flex flex-col h-full justify-center items-center
---

## OrbitGO

2025-04-04 ~ 2025-04-06

- 🥈 榮獲 ETHGlobal Taipei 2025 黑客松 1inch 賽道第二名
- 整合 1inch Portfolio API，實作多鏈資產查詢與視覺化介面

<div class="text-blue-400">https://orbitgo.calpa.me/</div>

::right::

![1inch 賽道銀獎](https://assets.calpa.me/ethglobal-taipei-2025-1inch-best-portfolio-tracker.avif)

---
layout: two-cols
layoutClass: gap-4 bg-[#172966]
class: flex flex-col h-full justify-center gap-4 text-white
---

## 技術博客

2017 ~

- 持續分享前端、後端與 Web3 技術文章與實作心得，涵蓋 Astro、React.js、TypeScript 等主題
- 2025 年 3 月中開始每日一篇鐵人賽
- 2017 起累積 276 篇文章

<div class="text-blue-400">https://calpa.me/</div>

::right::

![Calpa 2025 Blog](https://assets.calpa.me/calpa-2025-blog.avif)

---
layout: two-cols
class: flex flex-col h-full justify-center items-center
---

## 紫微斗數排盤系統

2025-05-22 ~

https://calpa.me/tools/ziwei/

::right::

<img src="https://assets.calpa.me/紫微斗數排盤系統.avif" class="w-full my-4 object-contain mx-auto" />

---
layout: center
class: bg-[#172966] text-white
---

## 今天不只是 Demo，而是...

> 帶你實際走一遍「從想法到 App」的完整流程！

這場分享，會給你：

- 一套實用的 AI Prompt 寫法
- 一個 Bolt.new 的 App 實作框架
- 一次動手打造 3 款 App 的實戰體驗

🎯 目標：讓你以後只要幾分鐘，就能把點子變 App！


---
class: flex flex-col h-full justify-center items-center gap-4
---

<SDLC />

---
layout: center
---

## Bolt.new

<img src="https://assets.calpa.me/bolt_new_homepage.avif" class="w-3/4 my-4 object-contain mx-auto" />

---
layout: center
---

<Card>
  <!-- 標題 -->
  <div class="text-2xl">
    Bolt.new 的六大好處
  </div>

  <div class="grid grid-cols-2 md:grid-cols-3">
    <div class="cell">使用 Claude 模型理生成網站</div>
    <div class="cell" style="animation-delay: 300ms;">瀏覽器內直接全端開發</div>
    <div class="cell" style="animation-delay: 600ms;">整合 Netlify、Supabase 等服務</div>
    <div class="cell" style="animation-delay: 900ms;">由 StackBlitz 團隊打造</div>
    <div class="cell" style="animation-delay: 1200ms;">可以安裝 npm 各種套件</div>
    <div class="cell" style="animation-delay: 1500ms;">提供各種常見模板 (Astro, Next.js, React.js, Vue.js, Svelte.js)</div>
  </div>
</Card>


<style>
  .cell {
    @apply flex items-center justify-center p-4 border border-slate-400 text-black;
    @apply animate-fade-in;
    @apply animate-mode-backwards;

    @apply bg-green-600 text-white;
  }
</style>
---
layout: center
---

<Card>
  <!-- 標題 -->
  <div class="text-2xl">
    Bolt.new 最適合打造哪些類型的 App？
  </div>

<div class="grid grid-cols-2 md:grid-cols-3">
  <div class="bg-red-600 column">專業落地頁</div>
  <div class="bg-sky-600 column" style="animation-delay: 300ms;">創作者線上作品集</div>
  <div class="bg-indigo-600 column" style="animation-delay: 600ms;">工具 App</div>
  <div class="bg-pink-600 column" style="animation-delay: 900ms;">MVP</div>
  <div class="bg-yellow-500 column" style="animation-delay: 1200ms;">活動報名 App</div>
  <div class="bg-green-600 column" style="animation-delay: 1500ms;">生活習慣追蹤 App</div>
</div>
</Card>


<style>
  .slidev-layout {
    @apply p-0;
  }

  .column {
    @apply flex items-center justify-center p-4 border text-white;
    @apply animate-fade-in;
    @apply animate-mode-backwards;
  }
</style>

---
layout: center
---

## 實作時間

---
layout: center
class: bg-[#172966] text-white
---

<Card padding="8">
<h2>⚡ 請務必先註冊 Bolt.new</h2>

為了接下來的實作，請用這個連結加入：

<div class="text-yellow-300 text-lg font-bold">
  https://bolt.new/?rid=z0x4lz
</div>

- 免費領取 200K tokens
- 解鎖完整功能，不會卡在邀請頁
- 升級 Pro 還能你我都拿 5M tokens 🎁

<div class="text-sm text-white/60 mt-4">
已有 <span class="text-yellow-300 font-bold text-lg">15</span> 位朋友 透過這個連結加入，謝謝大家的支持！
</div>
</Card>

---
layout: center
class: bg-[#172966] text-white
---

<Card padding="8">
  <div class="text-2xl font-bold text-center leading-snug">
    💡 精選回應
  </div>

<v-click>
<div>
1️⃣「想做一款能追蹤每日飲食與情緒的小工具」<span class="text-xs text-yellow-300">（養成健康習慣從記錄開始）</span>
</div>
</v-click>

<v-click>
<div>
2️⃣「打造給孩子用的教育 App，紀錄學習過程與成長」<span class="text-xs text-yellow-300">（爸爸媽媽的數位育兒筆記 📒）</span>
</div>
</v-click>

<v-click>
<div>
3️⃣「幫助自己團隊管理任務的 AI 待辦清單」<span class="text-xs text-yellow-300">（幫你追進度，也幫你追老闆）</span>
</div>
</v-click>

<v-click>
<div>
4️⃣「我不想再複製貼貼筆記，想要筆記自動分類整合」<span class="text-xs text-yellow-300">（懶人筆記救星，AI 排好一切）</span>
</div>
</v-click>

<v-click>
<div>
5️⃣「地鐵導航 App，不用再問路就能知道哪個出口」<span class="text-xs text-yellow-300">（出口8號，不是恐怖遊戲那個啦）</span>
</div>
</v-click>

<v-click>
<div>
6️⃣「設計給長輩使用的吃藥提醒 App，簡單、清楚最重要」<span class="text-xs text-yellow-300">（不只是提醒，更是一種陪伴）</span>
</div>
</v-click>

<v-click>
<div>
7️⃣「做個記帳＋財務預測的工具，讓錢不再神隱」<span class="text-xs text-yellow-300">（花在哪、賺多少，一清二楚）</span>
</div>
</v-click>

<v-click>
<div>
8️⃣「我真的每天都在想午餐吃什麼，想做『午餐決策 App』」<span class="text-xs text-yellow-300">（今天吃什麼？AI 來決定 🍜）</span>
</div>
</v-click>

<v-click>
<div>
9️⃣「其實我沒有明確想法，但就是想學會怎麼把 idea 實現！」<span class="text-xs text-yellow-300">（這場講座就是為你準備的 💡）</span>
</div>
<div class="text-xs text-yellow-300"> 🎤 你也可以思考：哪一類是你的共鳴呢？</div>
</v-click>
</Card>

---
layout: center
class: bg-[#172966] text-white
---

## 🗳 Voting Time！請到 Discord 投票！

<div class="text-xl mt-4">你最想看哪一款 App 的現場實作？</div>

1️⃣ 飲食情緒追蹤 App  
2️⃣ 教育紀錄 App  
3️⃣ AI 待辦清單  
4️⃣ 自動整理筆記  
5️⃣ 地鐵導航 App  
6️⃣ 吃藥提醒 App  
7️⃣ 財務記帳 App  
8️⃣ 午餐決策 App  
9️⃣ 學習如何實現 idea

<div class="text-yellow-300 text-sm mt-6">
📍 請到 Discord 的 <code>#2025-05-24</code> 頻道，對應貼上你的 emoji，例如 1️⃣ 2️⃣...
</div>

---

<LoadingScene isDebute />

---
class: flex flex-col h-full justify-center items-center gap-4
---

<Events filter="future" />

---
layout: two-cols
class: flex flex-col h-full justify-center
---

## 📍 5/30（台中）

Vibe Coding 工作坊

🧪 半天帶你從 0 到部署，親手打造自己的第一個產品！
✨ 適合沒寫過程式、但想做產品的人

🛠 使用工具：Cursor + Supabase + Zeabur

👥 小組協作、當場實作與展示

🗓 時間：5/30（五）13:30 – 18:00
📍 地點：台中 Monospace（台灣大道二段2號16樓之2）

🎟 報名連結：
👉 https://go.calpa.me/2025-05-30

::right::

<img src="https://assets.calpa.me/2025-05-30-banner.avif" class="w-full my-4 object-contain mx-auto" />


---
layout: two-cols
class: flex flex-col h-full justify-center
---

## 📍 6/1（台北）

《AI 煉金術》實體分享會

- 從靈感到 Side Project，用 AI 工具煉出你的創作流程
- 工具包含 ChatGPT、Firecrawl、Notion
- 分享我從 prompt → 文章 → 產品的完整流程

📅 時間：6/1（週日）15:00 – 18:00

📍 地點：小樹屋｜龍眼 501
- 捷運西門站 3 分鐘
- 台北市萬華區成都路67號5樓之1-501房

🆓 免費參加

📌 報名表單：
👉 https://go.calpa.me/2025-06-01

::right::

<img src="https://assets.thehapp.com/jZOMrUk.jpg" class="w-full my-4 object-contain mx-auto" />

---

## 謝謝大家

<img src="https://assets.calpa.me/感謝您讓我占用的寶貴時間.avif" class="w-2/3 my-4 object-contain mx-auto" />


<div class="text-sm text-white/60 mt-2">💬 想繼續交流、也歡迎私訊我或加入 Discord 群組！</div>

<div class="text-xs text-white/60 mt-2">© Calpa Liu. All rights reserved.</div>

