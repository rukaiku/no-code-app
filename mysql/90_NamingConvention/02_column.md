# カラム命名規約

## 概要

このドキュメントでは、データベースのカラム名に関する命名規約を定義する。  
命名規約を統一することで、データベースの可読性と保守性を向上させる。

## 命名規約

### プレフィックス

カラム名には、特定のプレフィックスを付けることは推奨されない。ただし、特定の用途に応じて一貫性を持たせること。

### 単数形

カラム名は単数形を使用する。例えば、ユーザーIDカラムは`user_id`とする。

### スネークケース

カラム名はスネークケース（小文字とアンダースコア）を使用する。例えば、`created_at`。

### 意味のある名前

カラム名はその内容を明確に示す意味のある名前にする。例えば、`created_at`は作成日時を示す。

### データ型に依存しない名前

カラム名はデータ型に依存しない名前にする。例えば、`amount`は`amount_int`や`amount_float`ではなく、単に`amount`とする。

## 例

| カラム名           | 説明                     |
|--------------------|--------------------------|
| `user_id`          | ユーザーID               |
| `role_id`          | 権限ID                   |
| `created_at`       | 作成日時                 |
| `updated_at`       | 更新日時                 |
| `created_by`       | 作成ユーザー             |
| `updated_by`       | 更新ユーザー             |

## 注意事項

- カラム名は一意でなければならない。
- カラム名の変更は、影響範囲を十分に確認した上で行うこと。

以上が、カラム名に関する命名規約である。この規約に従って、データベースのカラムを作成すること。
