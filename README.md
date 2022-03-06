# OpenGLで地形描画
2021年7月、計算機実践演習の課題で作成した。7月16日の発表会では70人ほどのA班の中で一位を頂いた。

## これは何？
国土地理院が公開しているDEM(数値標高モデル)のごく一部を加工しOpenGLを用いてメッシュで描画した。
[DEMダウンロードページ](https://fgd.gsi.go.jp/download/mapGis.php?tab=dem)　*ただし登録が必要である。

プログラムを実行すると下図右半分のように地形を描画することが出来る。左半分は作者が実際に現地に向かい撮影した写真であり、これに画面キャプチャしたものを合成した。
![drawer_background](https://user-images.githubusercontent.com/83338859/156910419-ac77e475-2438-452b-9614-1d5225cf0aac.png)

## できること
１，メッシュで上図のように地形を描画し、キー入力で空間内を移動・回転をすること

２，加工したGPXデータを地形上に赤線でプロットし自動で再生、そして変化する緯度・経度・高度・速度・時間・勾配などの情報を表示すること(下図参照)
![Screenshot from 2021-07-15 03-14-05](https://user-images.githubusercontent.com/83338859/156910730-bbb5518b-9c78-419f-b921-bafacdab5a1d.png)

## 実行
詳細なファイルの説明はreadme.txtを見て欲しい。main.cが地形描画プログラムでありその他はデータ加工のためのプログラムである。
実行にはOpenGLが必要。コンパイルは以下のように行う。
```
gcc main.c -o main -lglut -lGLU -lGL -lm
./main
```
