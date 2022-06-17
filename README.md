# build_corpus_sandbox

- dump データの取得方法に関して
    - https://ja.wikipedia.org/wiki/Wikipedia:%E3%83%87%E3%83%BC%E3%82%BF%E3%83%99%E3%83%BC%E3%82%B9%E3%83%80%E3%82%A6%E3%83%B3%E3%83%AD%E3%83%BC%E3%83%89

```
curl https://dumps.wikimedia.org/jawiki/latest/jawiki-latest-pages-articles.xml.bz2 -o jawiki-latest-pages-articles.xml.bz2
python -m wikiextractor.WikiExtractor jawiki-latest-pages-articles.xml.bz2
```
[Wikipedia:カテゴリ - Wikipedia](https://ja.wikipedia.org/wiki/Wikipedia:%E3%82%AB%E3%83%86%E3%82%B4%E3%83%AA)
- 解答して raw な xml を取得する
    -  bunzip2 -k jawiki-latest-pages-articles.xml.bz2
- 整形してデータを取り出す
    - https://github.com/attardi/wikiextractor

# その他必要情報
- media wiki の format 
    - https://www.mediawiki.org/wiki/Help:Formatting

# 目的関連
- 産業と技術のカテゴリに関するページを取得したい
    - https://ja.wikipedia.org/wiki/Portal:%E6%8A%80%E8%A1%93%E3%81%A8%E7%94%A3%E6%A5%AD
- ex. 回生ブレーキのページ
    - https://ja.wikipedia.org/?curid=76544
- wikipedia の page の id の取得方法
    - https://sleepygamersmemo.blogspot.com/2017/06/wikipedia-url-shortener.html

# カテゴリの取得
- [Wikipedia:カテゴリ - Wikipedia](https://ja.wikipedia.org/wiki/Wikipedia:%E3%82%AB%E3%83%86%E3%82%B4%E3%83%AA)
- [カテゴリツリー - Wikipedia](https://ja.wikipedia.org/w/index.php?title=%E7%89%B9%E5%88%A5:%E3%82%AB%E3%83%86%E3%82%B4%E3%83%AA%E3%83%84%E3%83%AA%E3%83%BC&target=%E4%B8%BB%E9%A1%8C%E5%88%A5%E5%88%86%E9%A1%9E&mode=10&hideprefix=20&showcount=1&namespaces%5B0%5D=4&notranslations=)
- https://qiita.com/tekunikaruza_jp/items/93d3267a444acef470d9
    - Wikipediaのカテゴリはツリー構造になっておらず、有向非巡回グラフになっている点

# コーパス作成 例
- [Wikipediaからコーパスを作る - いっきのblog](https://kzkohashi.hatenablog.com/entry/2018/07/22/212913)
