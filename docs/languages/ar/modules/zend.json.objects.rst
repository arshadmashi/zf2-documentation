.. EN-Revision: none
.. _zend.json.objects:

كائنات JSON
===========

عند القيام بعملية ترميز "encoding" لكائنات فى لغة PHP لتصبح فى صيغة JSON
, كل الـ public properties الخاصة بهذا الكائن سيتم ترميزها لتصبح كائنات
JSON.

عملية فك ترميز "decoding" كائنات JSON تواجه بعض التحديات , لكن حيث أن
كائنات JavaScript تتشابه إلى حد ما مع الـ associative arrays الموجودة فى لغة
PHP , فتم أقتراح أن يتم تمرير معرف أسم class , ثم يتم إنشاء نسخة "instance"
من هذا الـ class و يتم تسكينه بأزواج من الـ key/value التى تم إستنباطها
من كائن الـ JSON , إلا أن البعض يشعرون بأن هذا من الممكن أن يتسبب
فى مخاطر امنية .

الإعدادات الأساسية لـ *Zend_Json* ستقوم بفك ترميز كائنات JSON و
تحويلها إلى associative arrays , و لكن إن كنت تود أن يتم إرجاع كائن ,
فيمكنك أن تحدد التالى :

.. code-block:: php
   :linenos:

   <?php
   // Decode objects as objects
   $phpNative = Zend\Json\Json::decode($encodedValue, Zend\Json\Json::TYPE_OBJECT);
   ?>
أى كائنات سيتم فك ترميزها , سيتم إرجاعها على أنها كائنات من
*StdClass* مع properties تتطابق مع قيم أزواج الـ key/value المستخلصة من صيغة
الـ JSON.

نصيحة إطار عمل Zend هى أن يقوم كل مبرمج بتحديد كيف سيقوم بفك ترميز
كائنات JSON , إن كان يجب أن يتم إنشاء كائن JSON من نوع محدد, فيمكن أن
يتم إنشائه من خلال أكواد المبرمج الخاصة ثم يتم تسكينه بالقيم
التى تم فك ترميزها بإستخدام *Zend_Json*.


