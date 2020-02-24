# PokemonBattleCalculator(PokeBaCa)

## 概要

ポケットモンスター剣盾　対人戦サポートツール

ポケモン対戦におけるポケモン選出を補助する

## 目標

1. ポケモンのタイプ相性を元に詰まない選出を勧める
2. 両パーティのすばやさを一覧にする
3. ステータスを元にダメージ期待値を表示

## 機能

- ログインせずに使える
- ポケモン
  - 実数値
    - 無振り, 極振り, 最低値(性格補正マイナス) の3つ
  - 努力値
    - 0, 252, +と-ボタンで(4...12...20...)と加算
  - 性格
    - おくびょう, ようき, ひかえめ, いじっぱり
    - その他の性格
      - A↑B↓, A↑C↓, ...
      - B↑A↓, B↑A↓, ...
      - 5 * 5マスの碁盤の目
  - もちもの
    - こだわり系, 襷, 球, チョッキ
    - きのみ系統はなし
  - わざ
    - わざの種類
      - レベルアップわざ
      - 遺伝わざ
      - わざマシン
      - わざレコード
      - 教えわざ
    - 攻撃技は威力80以上命中80以上でピックアップ
    - 攻撃技, 補助技でわける
- 両パーティ共通
  - パーティの弱点数をタイプごとに表示
    - 効果抜群: ○, 半減: △, 無効: ×
      - ○3, △1, ×1 など
  - わざの通りを可視化
    - わざ火力 * タイプ一致倍率 * タイプ相性 の値
    - <100: △, 100 - 150: ○, 150<: ◎
  - オーバーレイでポケモンを選択
    - 使用率ランキング降順, タイプ別
    - 最終進化系のみ
    - アイコンクリックで選択 選択済み一覧に表示
    - 選択一覧クリックで選択から外す
  - 素早さを順位化
- 自パーティ
  - 強制
  - せいかく, 努力値, わざ, もちもの の入力を求める

- 相手パーティ
  - マッチング時に入力 ポケモンの種類のみ
  
## タスク

### 必須

- ポケモンともちものアイコンを調達
- ポケモンのID, 種族値, タイプをデータベース化
- 防御タイプ(1, 2)を引数とし，[弱点, 等倍, 半減, 無効]を返すタイプ相性関数

### 任意

- ダメージ, ステータス実数値の計算関数
- マイパーティーを記録する
- 相手ポケモンの技候補を表示
