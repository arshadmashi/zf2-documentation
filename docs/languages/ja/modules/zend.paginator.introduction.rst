.. EN-Revision: none
.. _zend.paginator.introduction:

導入
==

``Zend_Paginator`` は、
データのコレクションにページを割り振ったりそれをユーザに表示したりするためのコンポーネントです。

``Zend_Paginator`` は次のような設計を目指しています。



   - リレーショナルデータベースに限らない任意のデータのページ処理

   - 表示しなければならないデータのみを結果から取得する

   - データの表示やページ処理コントロールのレンダリング方法を、
     特定のパターンのみに強制させない

   - ``Zend_Paginator`` と他の Zend Framework コンポーネントは疎結合にし、たとえば
     ``Zend_View`` や ``Zend_Db`` などと組み合わせて使用できるようにする




