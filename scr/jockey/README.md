# 騎手マスタ収集

## 準備

jockey_id ディレクトリに jockey_id.csv が存在しない場合には，
次を実行して騎手 ID を取得してください．

```sh
cd jockey_id
python main.py
```

## 実行

```sh
cd jockey_record
python main.py
```

取得に成功すると，"jockey_master.json"が生成されます．

## 出力形式

- 取得対象：現役，引退騎手
- 近走成績が 0 件の騎手の勝率と平均順位には 0 埋め
- 順位が数値でないものは除外
  (''(なし),'除','中','取','失','降','再')

## データ構造

```
[
    {
        "netkeiba_id":"５桁の騎手id(文字列型)",
        "name":"騎手名",
        "win_rate":"直近20件の勝率(小数)",
        "rank_average":"直近20件の平均順位(小数)"
    },
    {...},
    {...},
    ...
]
```
