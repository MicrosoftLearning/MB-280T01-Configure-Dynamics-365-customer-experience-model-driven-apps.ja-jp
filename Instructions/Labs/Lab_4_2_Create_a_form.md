---
lab:
  title: 'ラボ 4.2: フォームを作成する'
---

# ラボ 4.2: フォームを作成する

## シナリオ
Bellows 大学は、複数のキャンパスとプログラムを持つ教育機関です。 Bellow 大学の講師や管理者の多くは、イベントに参加したり、品目を購入したりする必要があります。 従来から、これらの経費を追跡することは困難でした。
キャンパス管理では、従業員に経費を報告するためのデジタルの方法を用意することにより、経費報告システムを最新化したいと考えています。
このコース全体を通じて、Bellows 大学の従業員が経費を管理できるようにするアプリケーションを構築し、自動化を実行します。

## ラボ手順の概要
このラボをきちんと修了すると、次をマスターできます。
- テーブル フォームをニーズに最適にカスタマイズする。

次のコンポーネントを操作します。
- フォーム: ここで、ユーザーはテーブル内の新しい行を作成または更新します。

## 前提条件
- モジュール 1 ラボ 0 - ラボ環境の検証の完了

## 演習 1:ビューとフォームのカスタマイズ
**目的:** この演習では、モデル駆動型アプリで使用されるカスタム作成されたテーブルのビューとフォームをカスタマイズします。

### タスク #1:経費精算書フォームの編集
1. まだサインインしていない場合は、`https://make.powerapps.com` にサインインします。
2. 環境がまだ選択されていない場合は、右上で経費明細書ソリューションをインポートした環境を選択します。
3. 左側のナビゲーションを使用して、**[ソリューション]** を選択します
4. 経費明細書ソリューションを開きます。
5. 経費明細書テーブルを見つけて開きます。
6. [データ エクスペリエンス] セクションで、**[フォーム]** を選択し、フォームの種類が [メイン] の "情報" フォームを開きます。 (重要: 必ずフォームの種類がメインのフォームを選択してください。)

**重要:** すべてのフォームの名前は既定で "情報" となっているため、選択したフォームが [メイン] という種類のフォームであり、それ以外ではないことを必ず確認してください。 既定では、フォームに "レポート名" と "所有者" という 2 つのフィールドがあります。

### タスク #2: フォームの列を選択する
1. 画面の右側の [プロパティ] パネルで、**"名前"** フィールドを選択し、それを "`Report Information`" に変更します。
2. 左側のナビゲーション ウィンドウから **[テーブル列]** を選択し、列をフォームにドラッグするか、単に列名をクリックして、"所有者" フィールドの下に以下のフィールドを追加します。
    - 説明
    - レポートの目的
    - レポートの期限
    - レポートの合計
3. **ステータスの理由**列をドラッグし、フォーム ヘッダーにドロップします。 ヘッダーはフォームの右上の領域です。 フォームのフィールドを表示するには、必要に応じて画面の右側にある [プロパティ] パネルを折りたたみます。
4. **[最終承認日]** 列をドラッグし、フォーム ヘッダーにある [ステータス] の横にドロップします。
5. **[所有者]** を選択します。 [プロパティ] パネルで、ラベルを *[`Requestor`]* に変更します。
6. 左側のナビゲーションを使用して、**[コンポーネント]** を選択します。
7. 1 列のセクションを選択して、現在のセクションの下に追加します。
8. [プロパティ] 画面で、ラベルを **[`Expense Lines`]** に変更します。
9. [経費行] セクションが選択されたままで、**"サブグリッド"** コンポーネントを見つけて選択します。
10. **[関連レコードを表示]** チェック ボックスをオンにします。
11. テーブルを **[経費行 (経費明細書)]** に設定します。
12. [既定] ビューを **[アクティブな経費行]** に設定します。
13. **完了** を選択します。
14. 右上の **[保存して公開]** ボタンを選択し、保存と公開が完了するまで待ちます。
15. 画面の左上にある [戻る] ボタンを選択します。 これで、[経費精算書] テーブルの [フォーム] に戻ります。

### タスク #3: アクティブな経費行フォームを編集する
このタスクでは、経費行項目の追加に使用するフォームを変更します。

1. まだサインインしていない場合は、`https://make.powerapps.com` にサインインします
2. 環境がまだ選択されていない場合は、右上で経費明細書ソリューションをインポートした環境を選択します。
3. 左側のナビゲーションを使用して、[ソリューション] を選択します
4. 経費明細書ソリューションを開きます。
5. 経費行テーブルを見つけて開きます。
6. [データ エクスペリエンス] セクションで、[フォーム] を選択し、フォームの種類が [メイン] の "情報" フォームを開きます。 (重要: 必ずフォームの種類がメインのフォームを選択してください。)

**重要:** すべてのフォームの名前は既定で "情報" となっているため、選択したフォームが [メイン] という種類のフォームであり、それ以外ではないことを必ず確認してください。 既定では、フォームに "経費のタイトル" と "所有者" という 2 つのフィールドがあります。

1. 画面の右側の **[プロパティ]** パネルで、**"表示名"** フィールドを選択し、それを "`Item Details`" に変更します
2. 左側のナビゲーション ウィンドウから **[テーブル列]** を選択し、列をフォームにドラッグするか、単に列名をクリックして、"所有者" フィールドの下に以下のフィールドを追加します。
    - 経費の種類
    - 項目の説明
    - 経費の金額
    - 経費精算書
3. **ステータスの理由**列をドラッグし、フォーム ヘッダーにドロップします。 ヘッダーはフォームの右上の領域です。 フォームのフィールドを表示するには、必要に応じて画面の右側にある [プロパティ] パネルを折りたたみます。
4. **保存して公開**ボタンを選択します。
