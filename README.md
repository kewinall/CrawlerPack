# 資料爬蟲包

公開於 JCConf 2015 TW 高效率資料爬蟲組合包 投影片 http://www.slideshare.net/ssuser438746/jcconf-2015-tw

### Maven import
    <dependency>
        <groupId>com.github.abola</groupId>
        <artifactId>crawler</artifactId>
        <version>0.9.2</version>
    </dependency>

### 簡易使用程式碼
    // 指定 URI format 來源
    String api = "https://raw.githubusercontent.com/abola/CrawlerPack/master/test.json";
    // 指定資料格式，使用CSS selector 來擷取資料
    CrawlerPack
        .getFromJson(api)
        .select("results name").text() ;

### 調整中項目 
* 在 http/https 中支援 cookie 


### Change log
#### 0.9.2
* 修正解析註解以及 js 中特殊符號的錯誤
* 修正動態網頁資料被cache的問題

#### 0.9.1
* 增加授權，使用Apache 2.0 公開授權
* 專案已上傳至公開的 Maven Repository 現在可以直接透過pom.xml使用爬蟲包
* 修正 https PKIX 驗證無法通過的問題

