---
title: "言語プロセッサについてまとめてみた"
date: 2020-01-30T19:09:53+07:00
images: ["/images/office.jpg"]
categories: [コンピュータシステム]
tags: [コンピュータシステム, 基本情報技術者試験]
authors: []
---

皆さんは自分の書いた言語をプログラミング言語がどのようにコンピュータに命令を送っているのか知っていますか？
その鍵を握るのが今回説明する言語プロセッサです。

<!--more-->

> ### 言語プロセッサとは

言語プロセッサとは、人間が書くプログラミング言語（原始プログラム）をコンピュータが実行できる機械語（目的プログラム）に変換することです。  
また、その機械語を実行可能状態にするにはリンカと呼ばれる工程が必要になります。

プログラミング言語は二種類あります。

- コンピュータが理解しやすい低水準言語
- 人間が理解しやすい高水準言語

機械語とは、0 と 1 で表される言語です。

> ### 言語プロセッサの種類

- **アセンブラ**  
  アセンブラ言語を機械語命令に翻訳するプロセッサです。アセンブラ言語とは、ほぼ機械語に直接対応するレベルのプログラムを人間が読み書きできるようにしたもので、低水準言語の一つです。アセンブラ言語の一命令が、機械語の一命令となります。

- **コンパイラ**
  C 言語や、Java などの高水準言語の原始プログラムを目的プログラムに翻訳するプロセッサです。また、ソースコードのプログラムを一度まとめてから機械語に翻訳するので効率がいいです。コンパイラルの多くは、プログラムの実行を高速化する最適化機能（オプティマイズ）があります。
  開発をしているとコンパイルエラーというエラーが出てしまった経験がある方もいるのではないでしょうか。そのエラーはこれを実行する時のエラーです。

- **インタプリタ**  
  インタプリタも、高水準言語で記述された原始プログラムを目的プログラムに翻訳するプロセッサですが、コンパイラと違うのは命令を一つ一つ実行していくことです。なので金毘羅に比べて翻訳時間は長くなります。例として PHP や Perl, JavaScript が挙げられます。

- **ジェネレータ**  
  ジェネレータとは、RPG に代表される方式で、パラメータを設定することでプログラムを生成してくれます。

> ### コンパイラによる実行工程

1. **字句解析**  
   　ソースプログラムを一文字ずつトークン（字句）ごとに分解します。

2. **構文解析**  
   　トークンが言語の仕様に反していないかをチェックします。

3. **意味解析**  
   　プログラムの手続きの矛盾をチェックします

4. **コード最適化**  
   　実行スピードを早くするためにコードサイズを小さくしたり、論理式の最適化を行ったりします。

5. **コード生成**  
   　機械語に変換します。

> ### まとめ

このように人間が書いたプログラムはコンピュータがわかるように翻訳され私たちの思い通りに実行されています。このことを理解していると、エラーの意味がしやすくなったりしますね。

> 参考文献
> https://www.weblio.jp/content/%E3%82%A2%E3%82%BB%E3%83%B3%E3%83%96%E3%83%AA%E8%A8%80%E8%AA%9E > https://www.gadgety.net/shin/tips/unix/compiler.html
