# store-locator

セルフカフェ公式サイト（selfcafe.jp）に iframe で埋め込む「近くのセルフカフェを探す」ページ。

- 店舗情報は selfcafe.jp の公開 REST（店舗案内）から毎回読み込む。座標は `index.html` 内の控え（無い店は国土地理院の住所検索で求める）
- 地図: Leaflet + 国土地理院 淡色地図 / 駅検索: HeartRails Express / 地名検索: 国土地理院 住所検索（いずれも無料・キー不要）
- `index.html` は生成物。元は selfcafe-automation の `web/store-locator/widget.html`、生成は `py scripts/store_locator_data.py`

埋め込み例:

```html
<iframe src="https://selfcafe.github.io/store-locator/" width="100%" height="860" style="border:0" allow="geolocation" loading="lazy" title="近くのセルフカフェを探す"></iframe>
```
