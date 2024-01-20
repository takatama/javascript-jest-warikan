# 割り勘計算

## ファイルの説明

- src
  - warikan.js : プロダクトコード
- tests
  - warikan.test.js : テストコード

## Visual Studio Code でのセットアップ

0. node を使えるようにしておく（Mac なら brew と nvm がオススメ）
1. Visual Studio Code を起動する。
2. `Ctrl + Shift + P`でコマンドパレットを開き、`git clone`と入力する。
3. repository URL に`https://github.com/takatama/javascript-jest-warikan`と入力する。
4. clone するディレクトリーを選択する。
5. `Ctrl + Shift + P`でコマンドパレットを開き、`term`と入力し、`Terminal: Create New Terminal`を選択する。
6. ターミナルで`npm install`を実行する。

## Visual Studio Code でのテスト実行

1. `Ctrl + Shift + P`でコマンドパレットを開き、`term`と入力し、`Terminal: Create New Terminal`を選択する。
2. ターミナルで`npm test`を実行する。

## 割り勘計算の仕様

次のステップに従って、JavaScript と Jest で割り勘計算アプリとテストを作成する。

### Step0

Jest でテストを実行できるようにする。

### Step1

請求金額 totalBill を、参加人数 members で割った金額を 1 円単位で計算する。また、割り切れない金額は幹事が得をする。

たとえば 3330 円を 4 名で割る場合、1 名当たり 833 円払い、幹事は 2 円もらう。

### Step2

参加者には、普通に払う人、多く払う人、少なく払う人がいる。普通に払う人に比べて、多く払う人は 1.5 倍、少なく払う人は 0.5 倍払う。

たとえば 3330 円を普通の人 2 名、多い人 1 名、少ない人 1 名で割る場合:

- 普通の人 833 円
- 多い人 1250 円
- 少ない人は 417 円
- 幹事は 3 円もらう

### Step3

10 円単位で計算する。

たとえば 3330 円を普通の人 2 名、多い人 1 名、少ない人 1 名で割る場合:

- 普通の人 830 円
- 多い人 1250 円
- 少ない人 420 円
- あまりが出ないので幹事はもらわない

## 参考資料

- [飲み会の割り勘ドメイン](https://github.com/j5ik2o/warikan-domain-java)
- [warikan](https://github.com/takatama/warikan)
