=========================
About XAML
=========================

:著者: 松居　友平

XAMLについて
==================

XAML(Extensible Application Markup Language)は,netオブジェクトのインスタンス化に使用される

* WPFユーザーコントロールのインスタンス化

* panel,Buttonなどのコントロールのアレンジ

XAMLの基礎
=====================

プロジェクトを作成した時に自動生成するXAML

.. code-block:: xml
   :linenos:
   :emphasize-lines: 4

   <Window x:Class="WpfTutorial5.MainWindow"
           xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
           xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
           Title="MainWindow" Height="350" Width="525">
       <Grid>
           
       </Grid>
   </Window>

上記のコードは要素が2つあるが、トップレベルの要素は下記しか無い

* Window

* Page(Windowに似ているがnavegate用のアプリケーションに使用される)

* Application(リソースやスタートアップの設定を定義する)

4行目にある

.. code-block:: XAML

           Title="MainWindow" Height="350" Width="525">

はプロパティと呼ばれ、Windowのタイトルと縦横の大きさを設定している

----------------------------
XAMLの名前空間
----------------------------

.. code-block:: xml
   :linenos:
   :emphasize-lines: 2,3

   <Window x:Class="WpfTutorial5.MainWindow"
           xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
           xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
           Title="MainWindow" Height="350" Width="525">
       <Grid>
           
       </Grid>
   </Window>

* http://schemas.microsoft.com/winfx/2006/xaml/presentation

   Core WPF名前空間。ユーザーインターフェイスを含む全てのWPFクラスを参照ｌする

* http://schemas.microsoft.com/winfx/2006/xaml

   XAML名前空間。