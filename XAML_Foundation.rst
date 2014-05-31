=========================
XAMLの基礎
=========================

:著者: 松居　友平

WPFとXAMLの関係性
=========================

* XAML = 「CLRオブジェクトのインスタンス生成」

   XAMLは、
   `CLR <http://www.atmarkit.co.jp/icd/root/90/14096290.html>`_
   におけるオブジェクトのインスタンスを生成するためのマークアップ言語。

.. note:: CLR(Common Language Runtime)

   .net Framework上でアプリケーションを実行するエンジン。
   様々な言語で書かれたプログラムはコンパイルされCLRで実行される。

* CLRオブジェクトとXAMLコードの双方向変換

   C#やVBで定義したオブジェクトは、XAMLで
   `永続化 <http://ja.wikipedia.org/wiki/%E6%B0%B8%E7%B6%9A%E6%80%A7>`_
   が可能。

.. code-block:: csharp
   :linenos:

   using System.IO;
   using System.Windows.Markup;
   
   namespace Sample
   {
     public class Point
     {
       public int X { get; set; }
       public int Y { get; set; }
     }
   }
   
   class Program
   {
     static void Main(string[] args)
     {
       var x = new Sample.Point { X = 1, Y = 2 };
   
       using (var stream = File.Open("test.xaml", FileMode.Create))
         XamlWriter.Save(x, stream);
     }
   }

上のC#のPointクラスは下のXALMのように永続化できる

.. code-block:: xml
   :linenos:

   <Point X="1" Y="2"
     xmlns="clr-namespace:Sample;assembly=SampleLibrary" />

XMLコードから復元することもできるが、XamlReader.Loadメソッドを用いる。

XALMの基礎
=======================

