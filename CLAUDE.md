# Angie Game — Cowork 工作說明

## 專案概覽

這是一個 HTML 小遊戲合集，部署在 GitHub Pages。
- **GitHub Repo**: https://github.com/phoenixchentw/angie-game
- **GitHub Pages**: https://phoenixchentw.github.io/angie-game/
- **本地目錄**: 這個資料夾（angie_game）就是 git repo 根目錄

## 現有遊戲清單

| 檔案 | 遊戲 |
|------|------|
| `bowling_game.html` | 保齡球遊戲 |
| `brick_game.html` | 打磚塊 |
| `fruit_game.html` | 水果遊戲 |
| `hoop_game.html` | 投籃遊戲 |
| `index.html` | 首頁（遊戲選單） |
| `map_game.html` | 地圖遊戲 |
| `math_game.html` | 數學遊戲 |
| `pinball_game.html` | 彈珠台 |
| `racing_game.html` | 賽車遊戲 |
| `safe_game.html` | 保險箱遊戲 |

## 如何同步 GitHub（拉取最新版本）

```bash
# 拉取最新版本（只讀，不需要 token）
git -C /path/to/angie_game pull origin main
```

**注意**：推送（push）需要 GitHub Personal Access Token。
設定方式：在 Cowork 對話中告訴我你的 token，我會用 `git push https://<TOKEN>@github.com/phoenixchentw/angie-game.git main` 推送。

## 如何新增遊戲

1. **寫新遊戲 HTML**：在這個目錄新增 `xxx_game.html`（純 HTML + CSS + JS 單檔）
2. **更新首頁**：修改 `index.html`，把新遊戲加入選單
3. **推送到 GitHub**：
   ```bash
   git add xxx_game.html index.html
   git commit -m "Add xxx game"
   git push https://<TOKEN>@github.com/phoenixchentw/angie-game.git main
   ```
4. **GitHub Pages** 會自動部署（約 1-2 分鐘）

## 遊戲開發規範

- 每個遊戲都是**單一 HTML 檔案**（CSS 和 JS 都內嵌）
- 不需要外部框架，純 vanilla JS 即可
- 遊戲要有：開始畫面、遊戲畫面、結束/分數畫面
- 畫布建議用 `<canvas>` 或純 DOM
- 要支援手機觸控（如果適合的話）

## 請 Cowork 新增遊戲的指令範例

- 「幫我新增一個貪吃蛇遊戲」
- 「新增一個太空射擊遊戲，並更新 index.html」
- 「把新遊戲推送到 GitHub，我的 token 是 ghp_xxx」

## Git 設定

```
remote.origin.url = https://github.com/phoenixchentw/angie-game.git
branch = main
```
