# Adapter パターン
提供されているものがそのまま使えない疎きに、必要な形に変換してから利用する。
- すでに提供されているもの
- 必要なもの
のずれを埋めるようなデザインパターン

Wrapperと呼ばれることもある。

Adapterパターンは2種類ある
- クラスによるAdapterパターン(警鐘を使ったもの)
- インスタンスによるAdapterパターン(移譲を使ったもの)

> すでに作られたクラスがあって、新しいインタフェース(API)に適合させる。と考えると、Adapterパターンと言うのは当たり前のことのように感じられます。しかし、私たちは、新しいインタフェース（API）に適合させようとするとき、つい既存のクラスのソースをいじって「修正」しようと考えてしまいます。「ここをちょいと変えればきっと仕事はおしまいだな」と考えてしまうのです。でもそれでは、動作テストが住んでいる既存のクラスを、修正後にもう一度テストしなければならなくなってしまいます。
> Adapterパターンは、既存のクラスには全く手を加えずに、目的のインタフェース（API）に合わせようとするものです。また、Adapterパターンでは、既存のクラスのソースコードプログラムは必ずしも必要ではありません。既存の
クラスの仕様だけがわかれば、新しいクラスを作ることができるのです。

# バージョンアップと互換性
ソフトウェアにはバージョンアップがつきものです。ソフトウェアをバージョンアップするときに問題になるのが「古い版との互換性」です。古い版を捨ててしまえればソフトウェアのメンテナンスは楽なのですが、いつもそれができるとは限りません。古い版と新しい版とを共存させて、しかもメンテナンスを楽に行うためにAdapterパターンがやくに立つことがあります。

例えば、今後は新しい版だけをメンテナンスしたいとします。その場合は、新しい版をAdaptee役にとし、古い版をTarget役とします。そして、新しい版のクラスを使って古い版のメソッドを実装するAdapter役のクラスを作るのです。

# かけ離れたクラス
もちろん、Adaptee役とTarget役の機能があまりにもかけ離れている場合には、Adapterパターンは使えません。

# 関連しているパターン
- Bridge パターン
- Decorator パターン

# 学んだこと
この章では、インタフェース（API）が異なっている2つの間に入って、そのずれを埋めるためのAdapterパターンについて学びました。継承をつかったものと、移譲をつかったものを紹介し、それぞれの特徴についてお話しました。
