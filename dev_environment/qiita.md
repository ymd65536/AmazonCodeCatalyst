# 検証！Amazon CodeCatalystのDev Environmentで快適なVSCode環境を構築してみる

## はじめに

この記事では
Amazon CodeCatalystのDev Environmentを使って、VSCodeの開発環境を構築する方法を紹介します。
主な内容としては実践したときのメモを中心に書きます。（忘れやすいことなど）
誤りなどがあれば修正していく想定です。

## AWS上で快適に開発したい

AWSのサービスを使ってアプリケーションを開発しているような場合、
AWSのサービスとの連携がしやすい環境を構築したいですよね。

たいていの場合は、Visual Studio CodeのようなIDEを使って開発したり
JetBrainsのIDEを使って開発したりすると思います。

AWSだったらCloud9を使えばいいじゃん！という意見もあるかもしれません。
が、使い慣れているIDEを使いたいという場合もあるでしょう。

（とはいえ、vimやemacs使いであれば、Cloud9でもそれらを使えるので、そういう場合はCloud9でもいいかもしれません）

IDEがネックにならないなら、他に何がネックになるかというとCloud9はEC2のコンピューティング料金とストレージ料金がかかるということです。

開発者としては開発環境を建てる際のコストを抑えたいということもありますが、インフラを意識せずに開発に集中したいということもあります。
（開発中にコンソールでなんとなく起動したEC2と同じコンピューティング料金が発生していると思うと少し鬱陶しいと感じてしまう。）

## Dev Environmentならなんかイイカンジになるかも

そこでAmazon CodeCatalystでは、Dev Environmentという機能を使うことで
AWS上でVisual Studio CodeなどのIDEを起動できます。

### 補足：他にはどんなIDEが使えるのか

Dev EnvironmentではVSCode以外にも以下のIDEが使えるようです。

- IntelliJ IDEA Ultimate
- GoLand
- PyCharm Professional

※[Creating a Dev Environment](https://docs.aws.amazon.com/codecatalyst/latest/userguide/devenvironment-create.html)より参照

## Dev Environmentの料金

Dev Environmentは時間という単位で課金されるため、一見してCloud9で発生するようなコンピューティング料金と同じに見えるかもしれませんが、明確な違いがあります。

## 参考

- [Amazon CodeCatalyst](https://aws.amazon.com/jp/codecatalyst/)
- [Creating a Dev Environment](https://docs.aws.amazon.com/codecatalyst/latest/userguide/devenvironment-create.html)
- [What is a devfile?](https://devfile.io/docs/2.0.0/what-is-a-devfile)
- [devfile.io](https://devfile.io/)
- [AWS-Black-Belt_2023_Amazon-CodeCatalyst-Dev-Environments_1231_v1](https://pages.awscloud.com/rs/112-TZM-766/images/AWS-Black-Belt_2023_Amazon-CodeCatalyst-Dev-Environments_1231_v1.pdf)
- [Amazon CodeCatalyst による開発環境の管理](https://aws.amazon.com/jp/blogs/news/managing-dev-environments-with-amazon-codecatalyst/)
