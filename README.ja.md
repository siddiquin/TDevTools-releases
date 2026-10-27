# TDevTools

**開発者向けの無料デスクトップツールキット。JSON、XML、スキーマ、API、エンコード、証明書のための47種類のツールを、macOS、Windows、Linuxで利用できます。**

[transposal.app](https://transposal.app) 提供

**言語:** [English](README.md) · [Español](README.es.md) · [Français](README.fr.md) · [Deutsch](README.de.md) · [Türkçe](README.tr.md) · [日本語](README.ja.md) · [简体中文](README.zh-CN.md) · [हिन्दी](README.hi.md)

> **🔒 すべてローカルで処理。データがコンピューターの外に送信されることはありません。** TDevToolsの処理はすべてお使いのコンピューター上で行われます。JSON/XMLファイル、トークン、鍵、証明書がアップロードされたり、分析サービスへ送信されたりすることはありません。アカウント登録や追跡もありません。URLの読み込み、APIへのテストリクエスト、サーバー証明書の取得など、ユーザーが要求した場合に限りインターネットへ接続します。それ以外のツールはオフラインで動作します。

## スクリーンショット

**JSON → JSON Schema:** サンプルデータからスキーマを推定します。

![JSONからJSON Schema](screenshots/json-to-schema.png)

**APIテスター:** リクエストを送信し、レスポンスをツリー、表、テキストで確認します。

![APIテスター](screenshots/api-tester.png)

**証明書インスペクター:** 証明書チェーンを確認し、証明書と署名を検証します。

![証明書インスペクター](screenshots/certificate-inspector.png)

## ダウンロード

最新バージョンは[リリースページ](https://github.com/siddiquin/TDevTools-releases/releases/latest)からダウンロードできます。

| システム | ダウンロードするファイル |
| --- | --- |
| macOS、Apple Silicon (M1–M4) | `TDevTools-<version>-arm64.dmg` |
| macOS、Intel | `TDevTools-<version>-x64.dmg` |
| Windows 10/11、64ビット | `TDevTools-Setup-<version>-x64.exe` |
| Windows 10/11、ARM | `TDevTools-Setup-<version>-arm64.exe` |
| Windows、ポータブル版 | `TDevTools-Portable-<version>.exe` |
| Linux、64ビット (x86_64) | `TDevTools-<version>-x86_64.AppImage` |
| Linux、ARM64 | `TDevTools-<version>-arm64.AppImage` |

**動作要件:** macOS 12 Monterey以降、Windows 10/11（64ビットまたはARM64）、または最近の64ビットLinuxディストリビューション（Ubuntu 20.04以降、Debian 11以降、Fedora 36以降など）。ディスクに約300 MB必要です。

## インストール

### macOS

1. お使いのMacに合った`.dmg`をダウンロードして開き、使用許諾契約に同意します。
2. **TDevTools**を**アプリケーション**フォルダーへドラッグし、ディスクイメージを取り出します。
3. 初回起動時、Appleの有料開発者証明書で署名されていないため、macOSがアプリを検証できないという警告を表示することがあります。これは想定された動作で、許可は一度だけ必要です。
   - **macOS 14以前:** FinderでTDevToolsを右クリックして**開く**を選び、もう一度確認します。
   - **macOS 15以降:** アプリを開こうとして警告が出たら**完了**を押します。**システム設定 → プライバシーとセキュリティ**を開き、TDevToolsのブロック通知の横にある**このまま開く**を選んで確認します。
4. 「TDevToolsは壊れているため開けません」と表示された場合は、まず公式の[リリースページ](https://github.com/siddiquin/TDevTools-releases/releases/latest)からダウンロードしたことを確認してください。その後、ターミナルで `xattr -dr com.apple.quarantine /Applications/TDevTools.app` を実行すると、このアプリのダウンロード隔離属性だけを解除できます。

### Windows

- **インストーラー:** `TDevTools-Setup-<version>-x64.exe`（ARM PCでは`arm64`）を実行し、ライセンスに同意して**インストール**を選びます。SmartScreenに「WindowsによってPCが保護されました」と表示されたら、**詳細情報 → 実行**を選びます。ユーザーアカウント内にインストールされるため、管理者権限は不要です。
- **ポータブル版:** `TDevTools-Portable-<version>.exe`を実行します。SmartScreenが表示された場合は、**詳細情報 → 実行**を選びます。

### Linux (AppImage)

適切なファイルをダウンロードし、**プロパティ → 権限**で実行を許可するか、`chmod +x TDevTools-*.AppImage`を実行します。ダブルクリックするかターミナルから起動します。起動しない場合、一部のディストリビューションではFUSE 2が必要です（Ubuntu/Debian: `sudo apt install libfuse2`、Ubuntu 24.04: `sudo apt install libfuse2t64`、Fedora: `sudo dnf install fuse-libs`）。Gear LeverやAppImageLauncherでアプリメニューに追加できます。

## 更新とアンインストール

新しいバージョンをダウンロードして同じ手順でインストールしてください。設定は引き継がれます。macOSでは「アプリケーション」のアプリを置き換え、Windowsでは新しいインストーラーを実行し、LinuxではAppImageを置き換えます。

- **macOS:** TDevToolsをゴミ箱へ移動します。設定も削除するには`~/Library/Application Support/TDevTools`を削除します。
- **Windows:** **設定 → アプリ → インストールされているアプリ**からTDevToolsをアンインストールします。設定も削除するには`%APPDATA%\TDevTools`を削除します。ポータブル版は`.exe`を削除するだけです。
- **Linux:** AppImageを削除します。設定も削除するには`~/.config/TDevTools`を削除します。

保存されるのはテーマや言語などの設定だけです。データ、パスワード、鍵のコピーは保存されません。

## 機能

- **フォーマットと検証:** JSONの整形、検証、修復、ビジュアル編集。JSON、XML、CSV、Excel、YAML、TOON、JSONLの変換。Markdown、JSON/XMLスキーマ（XSD）、TypeScript型の生成。
- **セキュリティ:** JWTのデコード、検証、署名。Base64/URL/SAMLのエンコード。MD5、SHA-1、SHA-256ハッシュ。自己署名証明書とmTLSキットの作成。証明書、公開鍵、JKSキーストアの検査。
- **表示とAPI:** JSONのツリー、表、グリッド、グラフ、Raw表示。OpenAPI/Swaggerビューアー、OAuth2とmTLS対応HTTPクライアント、SOAP/WSDLビューアー、ファイルビューアー、Markdownプレビュー。
- **検索と変換:** JSONPathテスター、正規表現による検索と置換、JavaScript/TypeScript/Python/C#にエクスポートできるJSONマッパー。任意利用のクラウドサービスTransposal Mapper。
- **比較:** JSON/XMLの構造比較、行単位のエラーを示すJSON Schema検証。
- **アプリ全体:** 8言語、6テーマ、アクセントカラー、表示密度とズーム、ワンクリックコピー、右クリックメニュー、ドラッグ＆ドロップ、ステータスバーのCPU/メモリ表示。

## プライバシーとセキュリティ

- すべての処理はローカルで行われ、貼り付けたデータや開いたファイルはアップロードされません。
- アカウント、テレメトリー、広告はありません。
- ネットワーク接続はURLの読み込み、APIテスト、証明書取得など、ユーザーが要求した場合に限られます。
- パスワード、トークン、秘密鍵はアプリ起動中のみメモリに保持されます。保存されるのは設定だけです。
- ウィンドウは分離され、厳格なコンテンツセキュリティポリシーを適用。HTMLプレビューではスクリプトを実行せず、プログラムやスクリプトを開く前に確認します。ログイン情報は選択したサーバー以外には送信されません。
- 組み込みサンプルは公開デモサーバーを使い、2分に1回までに制限されています。独自のURLやファイルには制限はありません。

## よくある質問

**TDevToolsは無料ですか？** はい、開発者向けに無料です。[ライセンス契約](LICENSE.md)をご覧ください。

**オフラインで使えますか？** はい。URL読み込み、API/SOAPテスト、証明書チェーン取得など、選択したサーバーとの通信を伴う機能を除き、オフラインで動作します。

**ソースコードは公開されていますか？** TDevToolsはクローズドソースです。件名を「TDevTools」として **<support@transposal.app>** へメールでお問い合わせください。

**インストール時に警告が出るのはなぜですか？** 有料のAppleまたはMicrosoft開発者証明書で署名されていないため、GatekeeperやSmartScreenが初回起動時に警告を表示します。インストール手順に従い、公式の[リリースページ](https://github.com/siddiquin/TDevTools-releases/releases/latest)からのみダウンロードしてください。

## ライセンスとサポート

- [エンドユーザー使用許諾契約](LICENSE.md): 無料で利用できます。保証はありません。契約全文はアプリの**ヘルプ → ライセンス契約**から8言語で確認できます。
- [サードパーティに関する通知](THIRD_PARTY_NOTICES.md)
- サポート: **<support@transposal.app>**
- Webサイト: [transposal.app](https://transposal.app)

© 2026 Transposal. All rights reserved.