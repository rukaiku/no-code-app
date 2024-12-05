# テーブル命名規約

## 概要

このドキュメントでは、データベースのテーブル名に関する命名規約を定義する。  
命名規約を統一することで、データベースの可読性と保守性を向上させる。

## 命名規約

### プレフィックス

テーブル名には、`xx_m_`または`xx_t_`のプレフィックスを付ける。`xx`は各システムの用途に基づき2文字で設定する。`m`はマスターテーブルを、`t`はトランザクションテーブルを示す。

| プレフィックス     | 説明                                 |
|--------------------|--------------------------------------|
| `cm_m_`            | 共通モジュールのマスターテーブル     |
| `cm_t_`            | 共通モジュールのトランザクションテーブル |
| `xx_m_`            | 各システムのマスターテーブル         |
| `xx_t_`            | 各システムのトランザクションテーブル |

### 単数形

テーブル名は単数形を使用する。例えば、ユーザーテーブルは`xx_m_user`とする。

### スネークケース

テーブル名はスネークケース（小文字とアンダースコア）を使用する。例えば、`xx_t_user_roles`。

### 意味のある名前

テーブル名はその内容を明確に示す意味のある名前にする。例えば、`xx_m_user`はユーザー情報を格納するマスターテーブルである。

## 例

| テーブル名         | 説明                                 |
|--------------------|--------------------------------------|
| `cm_m_user`        | 共通モジュールのユーザー情報を格納するマスターテーブル |
| `cm_m_role`        | 共通モジュールの権限情報を格納するマスターテーブル   |
| `cm_t_user_roles`  | 共通モジュールのユーザーと権限の関係を格納するトランザクションテーブル |

## 注意事項

- テーブル名は一意でなければならない。
- テーブル名の変更は、影響範囲を十分に確認した上で行うこと。

以上が、テーブル名に関する命名規約である。この規約に従って、データベースのテーブルを作成すること。