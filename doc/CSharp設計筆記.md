C#的設計筆記
----------


## 類別陣列



## 靜態類別與方法
如果將類別宣告為static,那麼就不需要宣告實驗即可使用. 通常我會用這個方法來做系統設定,這個範例是我在小幫手加的server config, 主要是用來指向不同的主機,以應付不同測試環境的需求,只要有新的測試主機要加,只要修改這個檔案即可.

[static class範例](https://bitbucket.org/tony62101/skis/src/c5b5d811bad270c1eb9b9766bc0c1e9168d3fcf0/%E7%AF%84%E4%BE%8B%E7%A8%8B%E5%BC%8F/static%20class%E7%AF%84%E4%BE%8B/ServerConfig.cs?at=master)


## 複製檔案

可以學到幾個重點

- 檔案路徑的使用
- 複製檔案

之前在設定檔案路徑時,會使用的方式為字串,然後要用特殊的方式來表式路徑. 但實際上C#的路徑設法有一定的方法,在結合檔名時也提供另一個方法來使用.

```
private string _sLocalPath = @"c:\skis\tampcheck";
private string _sFilename = "capicom.dll";
console.write(Path.Combine(_sLocalPath,_sFilename))
//output = c:\\skis\\tampcheck\\capicom.dll
```

其他可看[範例程式]()


