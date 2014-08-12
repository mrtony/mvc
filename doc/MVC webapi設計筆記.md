MVC的Webapi設計筆記
----------


#### 如何讓ApiController回傳我們指定的方式
ApiController類別的回傳值如果是JSON序列化字串,它會自動再幫倒忙加上'/',為了要XML-->JSON, 必需要有一些特殊的作法. 因為json.net在將XML轉為json字串後,不要再由webapi自動轉json回傳. 這裡示範手動回傳作法如下:

```
public HttpResponseMessage Get()
{
    JSON oJSON = new JSON();
    sJSON = oJSON.XMLToJSON(sXML);	//將XML轉為JSON字串
	var resp = new HttpResponseMessage(HttpStatusCode.OK);
	resp.Content = new StringContent(sJSON, Encoding.UTF8, "text/json");
	return resp;
}
```




```
http://localhost:50977/api/values?comp=8560&cosy=8560&sett=9801852
```