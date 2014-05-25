
=========================
参考
=========================

:著者: 松居　友平

rstの基礎
=================

----------------------
見出しのレベル
----------------------

見出しのレベル順::

   ====
   ----
   ####
   ****
   ^^^^
   ~~~~
   """"

-----------------------------
インラインマークアップ
-----------------------------

::

   ::

      **太字**
      
      *斜体*
      
      ``リテラル``
      
      `リンク付きテキスト <http://python.org>`_

------------------------------
コードブロック
------------------------------

::

   ::
   
      本ドキュメントはフィクションです。登場する人物、
      企業名は架空のものです。

::

   .. code-block:: python
   
      import this

``:linenos:`` を記述することでコードバングを表示

.. code-block:: reST

   .. code-block:: python
      :linenos:
   
      import this


.. code-block:: python
   :linenos:
   
   import this
   
   a = 1

インクルード
--------------------

別のファイルを挿入して、言語を指定することができる

.. code-block:: reST

   .. literalinclude:: example.rb
      :language: ruby
      :linenos:

特定の行をハイライト
-----------------------------

.. code-block:: reST

   .. code-block:: python
      :emphasize-lines: 3,5
   
      def some_function():
          interesting = False
          print 'この行はハイライトされます'
          print 'この行はされません'
          print '...でも、この行はされます'

--------------

.. code-block:: python
   :emphasize-lines: 3,5

   def some_function():
       interesting = False
       print 'この行はハイライトされます'
       print 'この行はされません'
       print '...でも、この行はされます'

関数を記述する
-------------------

::

   .. function:: open(file)
                 open(file, mode)
      :module: PIL.Image
   
      画像を開く。モードを指定するのであれば、必ず"r"を指定する。

------------------

.. function:: open(file)
              open(file, mode)
   :module: PIL.Image

   画像を開く。モードを指定するのであれば、必ず"r"を指定する。

-----------------------------
章や節に番号を振る
-----------------------------

``..toctree::`` に ``:numbered:`` を追加

::

   .. toctree::
      :maxdepth: 2
      :numbered:
   
      overview
      design
      implementation

---------------------------
図を挿入
---------------------------

図を挿入する
----------------------

::

   .. figure:: ファイル名
      :scale: 40%
      :alt: Alternate Text (これはキャプションではなくalt属性です)
   
      一行あけてここに書いたものがキャプションになります。

画像の大きさを変える
------------------------

*height

   縦の長さを指定する

*width

   横の長さをサイズか現在の行の幅から割合で指定する

*scale

   倍率を指定する

.. code-block:: reST

   - scaleを使った場合
   
   .. image:: ../img/python-logo-master-v3-TM.png
      :scale: 60
   
   - widthを割合で指定した場合
   
   .. image:: ../img/python-logo-master-v3-TM.png
      :width: 50%
   
   - heightとscaleを同時に指定した場合
   
   .. image:: ../img/python-logo-master-v3-TM.png
      :height: 50px
      :scale: 120% 

リンクを貼る
------------------

::

   .. image:: ../img/python.png
      :target: http://python.org

-----------------------
リスト
-----------------------

::

   * 那須塩原市
   * 真岡市
   
   1. まさし
   2. みんみん
   #. 夢餃子(#を使うと、自動で数字が割り当てられます)
   
   餃子
      宇都宮の名物として有名。餃子の像もある。静岡の浜松がライバル。
   ジャズ
      宇都宮はジャズの町としても売り出し中。
      楽器メーカーを多数抱える静岡の浜松がライバル
   焼きそば
      知る人ぞ知る宇都宮の名物。専門店多数。なぜかビニール袋で持ち帰る。  

-----------------------
表
-----------------------

::

   =========== ==================================
   勉強会で使う本
   ----------------------------------------------
   言語        本の名前
   =========== ==================================
   Ruby        dRubyによる分散・Webプログラミング
   Python      集合知プログラミング
   Objective-C 詳解Objective-C 2.0
   =========== ==================================

