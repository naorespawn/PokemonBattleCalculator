# PokemonBattleCalculator(PokeBaCa)
## 概要
ポケットモンスター剣盾　対人戦サポートツール
## 目的
対戦中に必要となる情報を一挙にする
## 機能
- ログインせずに大体の機能を使える
- 自パーティ
  - 努力値, 性格, もちもの から実数値を表示
- 対戦相手のポケモンをプルダウンメニューから選択する
  - 使用率ランキング順にソート 最終進化系のみ
- 素早さリストを表示
- 両パーティの弱点数をタイプごとに表示
- 自ポケモンをクリックすると，相手ポケモンにどの技が何%入るか表示
## タスク
### 必須
- ポケモンともちものアイコンを制作　もしくは調達
- 種族値をデータベース化
- 実数値(最低値, 無振り, 252振り, 極振り)をデータベース化
- ダメージ計算式, ステータス実数値計算式をモジュール化する
- [与えるタイプ, 受けるタイプ(1, 2)]を引数とし，[弱点, 等倍, 半減, 無効]を返すタイプ相性を計算
### 任意
- マイパーティーを記録する
- 相手ポケモンの技候補を表示
