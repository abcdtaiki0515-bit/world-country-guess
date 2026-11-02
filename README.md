# WORLD GUESS — 世界196か国を当てよう

ブラウザだけで遊べる無料の国当てゲーム。国連加盟193か国＋バチカン市国・パレスチナ・台湾を対象とし、196の一意な国コードで管理します。政治的な承認を示すものではありません。

## 公開・更新
GitHub Pages: mainブランチのルート `/` を公開。index.html（UI）、engine.js（判定）、assets/countries.json（国データ）、assets/world.json（地図）を編集してmainへコミットすると再公開されます。外部ビルドやAPIキーは不要です。

## 検証
`node test.cjs`：全196か国の到達、全分岐の非空・重複なし・最大8回答、旗コード、データ必須項目、広告属性を検査。ブラウザではPCと幅360/390/768pxの検証画面を用意。実機iPhone/Androidでのタッチ操作は別途確認が必要です。

## データ
取得日2026-11-02。mledoze/countries（ODbL 1.0）、GeoNames countryInfo（CC BY 4.0・人口の統計年は混在）、Natural Earth / world-atlas 50m（public domain）。mledozeのunMemberにはVATが含まれていたため明示的に除外し、193＋3で再構成。首都の一部は日本語、その他は原綴りです。人口は最新推計とは限りません。
https://github.com/mledoze/countries
https://download.geonames.org/export/dump/countryInfo.txt
https://github.com/topojson/world-atlas
https://www.naturalearthdata.com/

地図に形状が存在しない小国は中心座標の丸印で表示（一覧はtest-results.json）。小国も丸印と国名一覧で識別できます。境界線や海外領土の表記には地図資料固有の差異があり、回答時は一覧を優先してください。国の形のデータはISO数値コードで対応します。

## ライセンス
D3・TopoJSON：ISC（assets/LICENSE-*）。国データ：ODbL（assets/LICENSE-countries）。GeoNamesの人口を組み合わせたデータの出典は上記、派生countries.jsonはODbLに従って提供します。独自のUI・判定コードはMIT License（LICENSE）。

## 広告
楽天ふるさと納税のPRを説明欄と結果下部に表示。提供されたアフィリエイトURLのID・クエリをそのまま使用。公式広告HTML全体は未提供のため独自カードを使用。価格表示なし。成果計測・承認は楽天側の条件に依存し、購入テストは実施していません。
