MVC-開發過程的問題
--------

1. **為何使用Nuget套件還原,無法將jQuery或jQueryMobile的js及css檔案還原至content和scripts的檔案夾中?**

因為Nuget只會還原package檔案夾中的套件檔案,而不會還原至專案中的檔案夾. 因此要手動的來maintain曾經安裝過的檔案到content和scripts的檔案夾中。 可參考[這篇](http://nuget.codeplex.com/workitem/2094)
2. 