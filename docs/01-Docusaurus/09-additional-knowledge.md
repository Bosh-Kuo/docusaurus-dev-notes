---
title: Docusaurus 學習過程中的額外知識收集
sidebar_label: 補充知識
description: Docusaurus 專案 - 補充知識
last_update:
  date: 2023-02-20
keywords:
  - Docusaurus
  - SPA
  - nvm
  - npm
  - yarn
  - npx
  - Jamstack
  - Mdx
  - GoDaddy
tags:
  - Docusaurus
---


## **SPA**
<details>
  <summary>
    什麼是 Single-page application (SPA)?
  </summary>

單頁應用程式 `(Single-page Application, SPA)` 是一種 Web 應用程式，它只使用一個 HTML 頁面呈現所有內容。**當使用者與應用程式互動時，頁面不會完全重新載入，而是透過 JavaScript 動態地更新內容**。這有助於提高使用者體驗，因為頁面載入速度更快，並且不會中斷使用者操作。

與傳統的多頁應用程式不同，單頁應用程式通常使用 `AJAX` 和 `JavaScript` 實現前端路由，以實現不同的頁面切換而不重新載入整個頁面。這可以提高使用者體驗和應用程式的效率，因為這樣可以省去不必要的頁面重新載入，從而減少網絡流量和提高頁面加載速度。此外，單頁應用程式通常也支持離線操作，這對於使用者在無網絡連接時也能使用應用程式是非常有益的。

`AJAX (非同步 JavaScript 和 XML)` 和 JavaScript 是前端開發技術，但在實現上有所不同。**AJAX 是一種不重新載入整個頁面的情況下與伺服器通訊的技術**。它使用 JavaScript 發送 HTTP 請求，從伺服器獲取數據，並在頁面上動態更新內容。**JavaScript 是一種客戶端腳本語言，用於實現頁面上的互動和動態效果**。它可以通過 DOM (文檔對象模型) 操作 HTML 元素，實現頁面的動態更新。

因此，我們可以說，AJAX 是用於不重新載入整個頁面的情況下與伺服器通訊的技術，而 JavaScript 則是用於實現頁面互動和動態效果的腳本語言。在單頁應用程式中，AJAX 用於後端數據互動，JavaScript 用於前端更新和實現路由。

</details>

<details>
  <summary>
    SPA 的優點與缺點有哪些？
  </summary>

`優點：`
1. 更快的用戶體驗：因為 SPA 只需在頁面上更新特定區域，而不需要重新加載整個頁面，因此可以提高用戶體驗的速度。
2. 更低的服務器負擔：因為 SPA 只需向伺服器發送少量數據，因此可以降低伺服器的負擔。
3. 更簡單的開發：因為 SPA 把所有的路由都實現在客戶端，因此可以簡化開發流程。

`缺點：`

1. SEO 難以實現：因為 SPA 只有一個頁面，搜索引擎爬蟲可能無法抓取所有內容，因此 SEO 可能更難實現。
2. 難以診斷問題：如果出現錯誤，可能比較難以診斷問題的根源，因為 SPA 把所有邏輯都實現在客戶端。
3. 增加了客戶端的負擔：因為 SPA 把所有路由實現在客戶端，因此可能增加客戶端的負擔。
   
</details>

<details>
  <summary>
    哪種類型的網站適合用 SPA？
  </summary>

單頁應用程式 (Single-page Application, SPA) 適合用於以下類型的網站：

1. 富互動頁面：如果網站需要大量的互動，例如拖曳、放縮和選擇，則 SPA 可以提供更快、更流暢的用戶體驗。
2. 即時應用：如果網站需要實時數據，例如聊天、實時協作和即時交易，則 SPA 可以提供更快的實時響應。
3. 移動應用：如果網站需要提供移動端用戶體驗，則 SPA 可以提供更快、更方便的移動端用戶體驗。
4. 內容密集型網站：如果網站的內容比較密集，例如在線商城、餐廳菜單和電影院預告，則 SPA 可以提供更快、更流暢的內容體驗。

</details>


## **nvm & npm & yarn**
<details>
  <summary>
    nvm 是什麼？
  </summary>

`nvm (Node Version Manager)` 是一個命令行工具，可以在同一個系統中管理多個 Node.js 版本。它允許您在不改變全局 Node.js 安裝的情況下，輕鬆切換不同版本的 `Node.js` 和 `npm`（Node Package Manager）。這對於開發人員來說非常方便，因為他們可以在不同項目之間切換不同版本的 Node.js，並保證不會與其他項目產生版本衝突。若偏好以 yarn 取代 npm 做套件管理，可以先切用 nvm 切換到使用的 Node.js 版本並執行以下指令安裝 yarn:
```bash
nvm use [version]
npm install -g yarn
```

在這個版本下安裝 yarn 後，你就可以使用 `yarn` 命令管理 npm 套件。
</details>

<details>
  <summary>
    常用的 nvm 指令
  </summary>

- **`nvm install <version>`**：安裝特定版本的 Node.js。
- **`nvm use <version>`**：切換到特定版本的 Node.js。
- **`nvm list`**：顯示當前系統中已安裝的所有 Node.js 版本。
- **`nvm current`**：顯示當前使用的 Node.js 版本。
- **`nvm alias <name> <version>`**：為特定版本的 Node.js 設置一個別名。
- **`nvm unalias <name>`**：刪除特定版本的 Node.js 的別名。
- **`nvm ls-remote`**：顯示可以安裝的所有 Node.js 版本。
- **`nvm deactivate`**：停用當前版本的 Node.js。
- **`nvm reinstall-packages <version>`**：重新安裝特定版本的 Node.js 中的所有 npm 套件。
- **`nvm unload`**：卸載 nvm 並返回到系統默認版本的 Node.js。

</details>


<details>
  <summary>
    yarn v.s npm 
  </summary>

`yarn` 和 `npm` 是 Node.js 的兩種包管理器。

npm 是 Node.js 的默認包管理器，並且隨著 Node.js 一起安裝。它可以用來安裝、升級、管理專案中使用的包。Yarn 是一個 Facebook 推出的替代 npm 的包管理器，具有比 npm 更快、更穩定、更可靠的特點。它使用自己的儲存庫和風格，但是可以完全兼容 npm，可以通過更改一些設定來使用 npm 儲存庫。

主要的差異點包括：

- `速度`：Yarn 可以在安裝包的時候更快的下載及安裝，因為它使用了自己的高效的儲存庫。
- `穩定性`：Yarn 可以保證在安裝相同版本的包時獲得相同的結果，即使是在不同的開發環境或時間。
- `可靠性`：Yarn 可以解決 npm 常見的一些問題，例如安裝錯誤或不完整的包等。

總的來說，Yarn 是一個比 npm 更快、更穩定、更可靠的包管理器，但是不是所有的專案都需要使用它，具體的選擇取決於您的需求和偏好。

</details>


<details>
  <summary>
    npx 跟 npm 有什麼不一樣？
  </summary>

`npx` 和 `npm` 是 Node.js 的兩種命令行工具。

**npm 是一個全局的包管理器**，它允許開發人員安裝、升級、管理 Node.js 專案中使用的包。它是隨著 Node.js 一起安裝的，並且可以透過命令行來運行。

**npx 是 npm 的一個工具**，它允許開發人員在不安裝任何全局包的情況下，透過命令行直接執行 npm 包。它可以確保在執行命令時使用的是該命令所需的版本，而不需要全局安裝任何版本。

例如，如果您需要在專案中執行某個命令，並且希望確保使用的是該命令所需的版本，您可以使用 npx 來執行，例如：

```bash
npx <command>
```

這將會確保在執行命令時使用正確的版本，並且不會對系統造成影響。

</details>


## **Others**
<details>
  <summary>
    什麼是 Jamstack ?
  </summary>

`Jamstack` 是一種網站架構模型，主要基於靜態網頁技術和 API，以提供快速、安全和可靠的網站體驗。Jamstack 的名稱是由`「JavaScript」、「APIs」和「Markup」`三個字母組成的。

**Jamstack 的網站在架設時會先預先生成所有頁面的靜態 HTML，再通過 API 來獲取動態內容。**當使用者請求網站時，瀏覽器直接載入預先生成的靜態 HTML，因此網站的顯示速度非常快。此外，因為靜態 HTML 可以直接存儲在 CDN 上，因此網站也具有很高的可靠性和安全性。

Jamstack 在適用對象上非常適合那些不需要頻繁更新或者大量的動態內容的網站，例如靜態網站、博客、個人網站、小型產品網站等。它提供了一個簡單、快速和可靠的網站開發架構，可以為開發人員和站點網站提供很大的優勢。

</details>


<details>
  <summary>
    什麼是 MDX ?
  </summary>

**`MDX` 是一種把 Markdown 和 JSX 混合在一起的語法，用於構建 React 網站。**它允許開發人員在 Markdown 文件中插入 React 組件，並在 Markdown 內容上進行互動和動態呈現。

MDX 允許開發人員以簡單、易讀的方式撰寫網頁內容，並可以使用 React 組件來增強內容的互動性和呈現效果。這種技術的優點在於，開發人員可以將內容和應用邏輯分離，使其易於維護和更新。MDX 的使用方式非常簡單，開發人員只需在 Markdown 文件中插入 JSX 語法即可，例如：

```markdown
# Hello, World!

<MyComponent />
```

在這個範例中，開發人員可以在 Markdown 文件中插入一個叫做 "MyComponent" 的 React 組件，以進行互動或呈現更加複雜的內容。由於 MDX 可以和多種靜態網頁生成器（如 Gatsby、Next.js 等）整合，因此可以運用在多種不同的 Jamstack 網站開發案例中。

</details>


<details>
  <summary>
    GoDaddy 的 DNS 設定中的 A 紀錄與 CNAME 紀錄的差別
  </summary>

A 記錄和 CNAME 記錄是兩種不同類型的 DNS 記錄，它們在功能和用途方面有所不同。

A 記錄（也稱為「地址記錄」）是一種 DNS 記錄，它將域名映射到特定的 IP 地址。因此，當訪問帶有 A 記錄的域名時，瀏覽器將根據 A 記錄提供的 IP 地址發送 HTTP 請求。例如，如果你想將 "**[www.example.com](http://www.example.com/)**" 指向 IP 地址為 "192.168.1.1" 的伺服器，你可以在 GoDaddy 中設定一個 A 記錄，將 "www" 子域名指向 "192.168.1.1"。

CNAME 記錄（也稱為「別名記錄」）是一種 DNS 記錄，它將一個域名映射到另一個域名。因此，當訪問帶有 CNAME 記錄的域名時，瀏覽器將按照 CNAME 記錄提供的域名發送 HTTP 請求。因此，如果若希望將自己的域名映射到特定的 IP 地址，則應使用 A 記錄。但是，如果您希望將您的域名映射到另一個域名，則應使用 CNAME 記錄。

在 GoDaddy 的 DNS 記錄列表中選擇的這個 CNAME 記錄的名稱為 `note`，資料為 `cname.vercel-dns.com`。這意味著您將 `note.boshkuo.com` 網域名稱映射到 Vercel 的 `cname.vercel-dns.com` 網域。

這意味著當用戶訪問 `note.boshkuo.com` 時，他們將被重定向到您在 Vercel 中指定的網域，並且 Vercel 將提供您的網站内容。

</details>


<details>
  <summary>
    為什麽網站的圖標或 logo 常使用 .svg 檔跟 .ico 檔?為什麼不是使用 .png 或 .jpg?
  </summary>

**1. 無損縮放：** SVG 可以無損縮放，而且不會失去畫質，這對於在不同大小和分辨率的設備上展示圖標或 logo 是非常重要的。相反，PNG 和 JPG 格式的圖像會因為放大或縮小而失去畫質。  
**2. 矢量圖形：** SVG 是矢量圖形格式，可以使用數學方程式描述圖像，而 PNG 和 JPG 是點陣圖形格式，需要在像素級別上描述圖像。因此，SVG 可以保持清晰，而且文件大小比 PNG 和 JPG 更小，加快了網站載入速度。  
**3. 多平台支持：** ICO 檔是 Windows 平台特定的圖標檔格式，可用於在不同的 Windows 軟體中顯示圖標，而 SVG 是一種跨平台的矢量圖形格式，可以在各種設備和瀏覽器中使用。

</details>