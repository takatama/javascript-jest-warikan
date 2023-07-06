# 割り勘計算

## ファイルの説明

- .gitignore : Gitで管理しないファイル。
- README.md : 本ファイル
- app
  - warikan.js : プロダクトコード
  - warikan.test.js : テストコード

## Visual Studio Codeでのセットアップ

0. nodeを使えるようにしておく（Macならbrewとnvmがオススメ）
1. Visual Studio Codeを起動する。
2. ```Ctrl + Shift + P```でコマンドパレットを開き、```git clone```と入力する。
3. repository URLに```https://github.com/takatama/javascript-jest-warikan```と入力する。
4. cloneするディレクトリーを選択する。

## Visual Studio Codeでのテスト実行

Visual Studio Codeを起動するたびに実施する必要があるので注意する。

1. ```Ctrl + Shift + P```でコマンドパレットを開き、```Tasks: Run Test Task```と入力する。
2. Visual Studio Codeの左端にフラスコアイコン（Test）が表示される。
3. テストを実行する。
4. テストの出力結果を参照したい場合は、コマンドパレットを開き、```python show test outputs```と入力する。

## 割り勘計算の仕様

### Step1
請求金額totalBillを、参加人数membersで割った金額を1円単位で計算する。また、割り切れない金額は幹事が得をする。

たとえば3330円を4名で割る場合、1名当たり833円払い、幹事は2円もらう。

### Step2
参加者には、普通に払う人、多く払う人、少なく払う人がいる。普通に払う人に比べて、多く払う人は1.5倍、少なく払う人は0.5倍払う。

たとえば3330円を普通の人2名、多い人1名、少ない人1名で割る場合: 
- 普通の人833円
- 多い人1250円
- 少ない人は417円
- 幹事は3円もらう

### Step3
10円単位で計算する。

たとえば3330円を普通の人2名、多い人1名、少ない人1名で割る場合: 
- 普通の人830円
- 多い人1250円
- 少ない人420円

## 参考資料
- [飲み会の割り勘ドメイン](https://github.com/j5ik2o/warikan-domain-java)
- [warikan](https://github.com/takatama/warikan)