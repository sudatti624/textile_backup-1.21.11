# Textile Backup Fork

このリポジトリは、[Textile Backup](https://github.com/Szum123321/textile_backup) を Minecraft Fabric 1.21.11 向けに更新した非公式 Fork です。

元プロジェクトの作者および配布元による公式リリースではありません。問題報告や問い合わせは、元プロジェクトではなくこの Fork の管理者へ行ってください。

既存の設定やワールドとの互換性を保つため、mod id は upstream と同じ `textile_backup` を維持しています。一方で、表示名とビルド成果物名は upstream 版と区別しやすいように `Textile Backup Fork` / `textile_backup-fork` にしています。

mod id が同じため、upstream 版 Textile Backup との同時導入は想定していません。

## 注意事項

本リポジトリはAIを使用しています。
ご使用の際は自己責任でお願いします。

本番サーバーで使用する前に、必ずテスト環境でバックアップ作成と復元を確認してください。

## 対応環境

- Minecraft: 1.21.11
- Mod loader: Fabric Loader 0.19.3 以上
- Java: 21 以上
- 必須mod: Fabric API、Cloth Config
- 任意連携: Mod Menu

## ビルド方法

```powershell
.\gradlew.bat build
```

Remap 済みの mod jar は `build/libs/` に出力されます。ファイル名は次の形式です。

```text
textile_backup-fork-3.1.3-fork+mc1.21.11.jar
```

## 機能

Textile Backup は、サーバー側でワールドバックアップを作成する Fabric mod です。圧縮バックアップの自動作成、古いバックアップの整理、サーバー再起動後のバックアップ復元などを行えます。

upstream から引き継いでいる主な機能:

- マルチスレッド圧縮
- 複数のアーカイブ/圧縮形式
- スケジュールによる自動バックアップ
- 古いワールドの復元ワークフロー
- 日数、個数、サイズによるバックアップ整理
- バックアップコマンド用のプレイヤー whitelist / blacklist
- サーバー側のみで動作

## Fork での主な変更

この Fork は、Minecraft Fabric 1.21.11 でビルドおよび実行できる状態を維持することを主な目的としています。

- Minecraft、Yarn、Fabric Loader、Loom、Gradle を更新
- 実際に使用している Fabric API モジュールに合わせて依存関係を調整
- Minecraft 1.21.11 の permission API に合わせてコマンド権限チェックを更新
- Fork と分かるように表示名とビルド成果物名を変更
- 圧縮系ライブラリを配布 jar に同梱するように調整

## ライセンスと帰属

元プロジェクト: [Szum123321/textile_backup](https://github.com/Szum123321/textile_backup)

元プロジェクトのライセンス: GPLv3

本 Fork も元プロジェクトのライセンスに従い、GPLv3 のもとで扱われます。ライセンス全文は [LICENSE](LICENSE) を参照してください。

このプロジェクトには、同梱ライブラリおよび一部参考実装があります。詳細は [Copyright_Notice](Copyright_Notice) を参照してください。
