# kuo

## 專案介紹

我就是想做個網站!!!

## 成品展示

[網站網址(host by heroku)](https://pythondiary-kuo.herokuapp.com/)
![](https://github.com/kuanglien/kuo/blob/master/index.png)

## 使用技術

工具名稱 | 用途
---------|----------
Python 3 | 不需要解釋
Flask(python)    | 幫助我建立伺服器
HTML/CSS  | 網頁表示和排版
Heroku   | 託管網頁
Github   | 存放原始碼
reurl.cc | 縮短網址產生器
bootstrap | Python 3 語法學習參考1
bootstrap glyphicons | Python 3 語法學習參考2下載標籤小圖
markdown | 用於github的標記式語言


## 程式碼片段

```python
@app.route("/")
def home():
    temp = glob.glob("articles/*")
    fill = []
    for t in temp:
        length = len(glob.glob(t + "/*.txt"))
        category = t.replace("articles/", "")
        f = (category, length)
        fill.append(f)
    return render_template("index.html", cat=fill)
```
