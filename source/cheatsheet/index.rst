
#############
Cheatsheet
#############

*************
はじめに
*************
From `official document <https://planset-study-sphinx.readthedocs.io/ja/latest/index.html>`_.

*************
見出し
*************

.. code-block:: none

   ##############
   部の見出し
   ##############
   部の紹介文

   **************
   章の見出し
   **************
   章の紹介文

   Section Level1
   ==============

   Level2
   ------

   Level3
   ^^^^^^
   
   Level4
   """"""

************
強調
************

============== ========== ==============
意味           表示       書き方     
============== ========== ==============
強調           *文字列*   \*文字列\*   
強い強調       **文字列** \*\*文字列\*\*
コードサンプル ``文字列`` \`\`文字列\`\`
============== ========== ============== 

************
引用
************

行の先頭をインデントすると, 引用になります.

.. code-block:: rst

    パラグラフ

        引用文

    パラグラフ

パラグラフ

    引用文

パラグラフ

ラインブロックで改行をそのまま出力します.

.. code-block:: rst

    | ラインブロックで,
    | 改行をそのまま
    | 出力します.

パラグラフ

    | ラインブロックで,
    | 改行をそのまま
    | 出力します.


********
リスト
********

.. code-block:: none

    * 1
    * 2
    * 3
    
        + 1
        + 2
        + 3
    
            - 1
            - 2
            - 3

* 1
* 2
* 3

    + 1
    + 2
    + 3

        - 1
        - 2
        - 3

**********
番号リスト
**********

.. code-block:: none

    1. 1
    2. 2
    3. 3
    
    8. 1
    #. 2
    #. 3
    
1. 1
2. 2
3. 3

8. 1
#. 2
#. 3

**************
コードブロック
**************

.. code-block:: none

    .. code-block: python

        import sys
        print sys.path

.. code-block:: python

   import sys
   print sys.path

対応言語の一部, ``c, c++, python``.
一覧は, `pygments ドキュメント <https://pygments.org/languages/>`_ で確認できます.

************
リンク
************

.. code-block:: none

   - http://sphinx-doc.org
   - `sphinx-doc <http://sphinx-doc.org>`_

- http://sphinx-doc.org
- `sphinx-doc <http://sphinx-doc.org>`_
- sphinx-doc-url_

.. _sphinx-doc-url: http://sphinx-doc.org

特殊なリンクとして, ダウンロード用リンクを作ることができます. _downloadsディレクトリが作成され, ダウンロード用のファイルが出力されます.

.. code-block:: none
   
   :download:`ダウンロード <index.rst>`

:download:`ダウンロード <index.rst>`


************
テーブル
************

.. code-block:: none

    ==== ==== ====
    col1 col2 col3
    ==== ==== ====
    row1 a    b
    row2 a    b
    row3 a    b
    ==== ==== ====

==== ==== ====
col1 col2 col3
==== ==== ====
row1 a    b
row2 a    b
row3 a    b
==== ==== ====

************
画像
************

パスはこのファイルからの相対パスです.

.. code-block:: none

    .. image:: result_ggx_vnd2_0.5_131072.jpg
       :scale: 25%

.. image:: result_ggx_vnd2_0.5_131072.jpg
   :scale: 25%

******************
警告ディレクティブ
******************

************
拡張
************

``sphinxcontrib.getstart_sphinx.column``
========================================

.. column:: コラムスペース

    コラムスペースです.
    コードブロックのように改行もそのままです.

