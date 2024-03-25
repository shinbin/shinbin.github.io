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


assetlinks.json 簽名用途依序為 : [google Play App 簽名], [key store 簽名] , [andy WIN11 PC debug臨時簽名], [mac debug 臨時簽名] ,
[ "60:98:86:19:F5:05:01:99:10:5A:0C:48:30:EB:20:68:63:0A:39:AF:BF:A5:4F:F2:61:95:F2:13:C5:6D:4F:01",
"6C:7F:51:AD:83:3D:97:9D:00:90:79:AC:A3:11:BE:54:A3:D8:14:16:1E:CF:22:D1:EA:FB:B1:66:F3:5A:DB:D5",
"E4:14:C8:10:F7:B9:CE:A5:13:6F:86:D4:D1:F5:4F:33:DC:A7:DC:23:D1:C8:3E:37:69:1C:F9:E6:C3:08:8C:0D",
"B2:14:19:3D:04:B5:A1:B7:AC:C1:07:EC:F6:BE:29:10:97:6A:DD:F8:3D:41:58:8F:EF:D5:E8:14:54:1D:E9:1A"
]