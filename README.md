# udn_news_money_rss_wordcloud

# 專案概要
從聯合新聞網(udn)的經濟新聞RSS (https://money.udn.com/rssfeed/news/1001/5588/10511?ch=money) 爬取最新文章內文，並根據文章內容生成文字雲，方便隨時監測熱門關鍵字。

文字雲(Word Cloud)，又稱詞語雲或標籤雲，是一種將文字數據可視化的方法。它通過將文字按照在數據中出現的頻率以不同大小和顏色展示在畫布上，使人們能夠直觀地了解文章中最重要和最熱門的詞語和主題。在這個專案中，文字雲對於快速識別新聞中的熱點話題和市場趨勢具有很高的價值。

使用Python編寫，使用了以下函式庫和工具：
- BeautifulSoup：用於解析RSS來源中的文章標題和連結
- lxml：用於解析文章內容
- jieba：用於分詞，並自定義過濾停用詞
- wordcloud：用於生成文字雲
- matplotlib：展示生成的文字雲圖片檔案
- Docker和docker-compose：用於建立和運行專案的容器環境

# 安裝方式
使用Docker和docker-compose進行部署，確保您已經安裝了Docker。
1. 從GitHub克隆Repo到本地。
```commandline
git clone https://github.com/estelladai/udn_news_money_rss_wordcloud.git
```
2. 進入專案目錄。
```commandline
cd udn-news-wordcloud
```
3. 建立Docker容器。
```commandline
docker-compose build
```

# 使用方法
1. 啟動Jupyter。
```commandline
docker-compose up -d
```
2. 查看Jupyter運行日誌，找到Jupyter啟動時生成的連結，連結包含一個token。
```commandline
docker-compose logs notebook
```
3. 打開瀏覽器，貼上剛才從日誌中獲取的連結(含token)，並進入Jupyter。
4. 在Jupyter中打開udn_news_wordcloud.ipynb文件，運行所有Cell生成文字雲圖片。
5. 查看生成的文字雲圖片，可以在work/udn_news_wc.png文件中找到。

# 新聞文字雲圖片
[新聞文字雲](work/udn_news_wc.png)
