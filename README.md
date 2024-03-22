# shinbin.github.io

.well-known >
             apple-app-site-association : iOS universal link 配置檔
             assetlinks.json ： Android app links 配置檔
ilabelprint >
             example.html : app links 範例頁面，ilabelprint＋ 範例連結
             print.html   : iOS universal link 連結頁面
labels >
         link_example.json : example.html 連結後會下載的標籤檔
index.html > 開發測試網頁 （不需要上正式環境）
debug.html > 開發測試網頁-debug mode （不需要上正式環境）


驗證AppLinks生效
Android : Command=> adb shell pm get-app-links com.argox.ilabel_print2 (https://developer.android.com/training/app-links/verify-android-applinks?hl=zh-tw)
          https://developers.google.com/digital-asset-links/tools/generator?hl=zh-tw

iOS : (1) 蘋果有 CDN，所以設定後需要數小時後才能動作，可以使用 https://app-site-association.cdn-apple.com/a/v1/shinbin.github.io 檢查是否已更新。
      (2) 將 print.html 暫時改名,讓URL 連不到出現404, 此時上方要出現 OPEN
   associated domains (test):   applinks:shinbin.github.io?mode=developer