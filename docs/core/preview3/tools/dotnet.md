---
title: "dotnet コマンド | .NET Core SDK"
description: "dotnet コマンド (.NET Core CLI ツールの一般的なドライバー) とその使用法について説明します。"
keywords: "dotnet, CLI, CLI コマンド, .NET Core"
author: blackdwarf
ms.author: mairaw
ms.date: 10/07/2016
ms.topic: article
ms.prod: .net-core
ms.technology: dotnet-cli
ms.devlang: dotnet
ms.assetid: 93015521-2127-4fe9-8fce-ca79bcc4ff49
translationtype: Human Translation
ms.sourcegitcommit: 1a84c694945fe0c77468eb77274ab46618bccae6
ms.openlocfilehash: bbc13c8cca82e660f0f8ccf7d88c0340d9c06e68

---

#<a name="dotnet-command"></a>dotnet コマンド

## <a name="name"></a>名前

dotnet -- コマンドラインのコマンドを実行するための一般的なドライバーです。

## <a name="synopsis"></a>構文

`dotnet [--version] [--verbose] [--info] [command] [arguments] [--help]`

## <a name="description"></a>説明
`dotnet` は、コマンド ライン インターフェイス (CLI) ツールチェーンの一般的なドライバーです。 単独で呼び出され、簡単な使用方法を説明します。 

特定の機能がそれぞれコマンドとして実装されます。 機能を使用するには、[`dotnet build`](dotnet-build.md) のように、`dotnet` の後にコマンドを指定します。 コマンドに続く引数はすべて独自の引数です。 

`dotnet` が単独でコマンドとして使用されるのは、ポータブル アプリを実行する場合にのみです。 アプリケーションを実行する場合は、`dotnet` の動詞の後にポータブル アプリケーション DLL を指定するだけです。    

## <a name="options"></a>オプション

`-v|--verbose`

詳細出力を有効にします。

`--version`

CLI ツールのバージョンを印刷します。

`--info`

現在のオペレーティング システム、バージョンのコミット SHA など、CLI ツールの詳細情報を印刷します。 

`-h|--help`

コマンドの短いヘルプを印刷します。 `dotnet` のみで使用すると、使用可能なコマンドのリストも印刷されます。  

## <a name="dotnet-commands"></a>dotnet コマンド

次のコマンドは dotnet のために存在します。

* [dotnet-new](dotnet-new.md)
   * C# または F# コンソール アプリケーション プロジェクトを初期化します。
* [dotnet-restore](dotnet-restore.md)
  * 指定されたアプリケーションの依存関係を復元します。 
* [dotnet-build](dotnet-build.md)
  * .NET Core アプリケーションをビルドします。
* [dotnet-publish](dotnet-publish.md)
   * .NET ポータブルまたは自己完結型アプリケーションを発行します。
* [dotnet-run](dotnet-run.md)
   * ソースからアプリケーションを実行します。
* [dotnet-test](dotnet-test.md)
   * project.json で指定されたテスト ランナーを使用してテストを実行します。
* [dotnet-pack](dotnet-pack.md)
   * コードの NuGet パッケージを作成します。
* [dotnet-migrate](dotnet-migrate.md)
   * 有効な Preview 2 プロジェクトを Preview 3 プロジェクトに移行します。
* [dotnet-msbuild](dotnet-msbuild.md)
   * MSBuild コマンドラインへのアクセスを提供します。

## <a name="examples"></a>例

コンパイルして実行できるサンプルの .NET Core コンソール アプリケーションを初期化します。

`dotnet new`

指定されたアプリケーションの依存関係を復元します。

`dotnet restore`

指定されたディレクトリにプロジェクトとその依存関係をビルドします。 

`dotnet build`

`myapp.dll` という名前のポータブル アプリを実行する: `dotnet myapp.dll`

## <a name="environment"></a>環境 

`DOTNET_PACKAGES`

プライマリ パッケージのキャッシュです。 設定されていない場合は、既定で $HOME/.nuget/packages (Unix の場合) または %HOME%\NuGet\Packages (Windows の場合) になります。

`DOTNET_SERVICING`

ランタイムの読み込み時に共有ホストで使用するサービス インデックスの場所を指定します。

`DOTNET_CLI_TELEMETRY_OPTOUT`

.NET Core ツールの使用に関するデータを収集し、Microsoft に送信するかどうかを指定します。 `true` の場合は、テレメトリ機能が無効になります (指定できる値は true、1、yes です)。それ以外の場合は `false` です (指定できる値は false、0、no です)。 設定されていない場合、既定で `false` (つまり、テレメトリ機能が有効) になります。




<!--HONumber=Nov16_HO3-->


