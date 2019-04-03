FrameData
======================

数据类型
~~~~~~~~~~

.. code:: java

    /**
     *
     * FrameData.COLOR
     * FrameData.DEPTH
     *
     * */
    public int flag;

图像宽度
~~~~~~~~~~

.. code:: java

    public int width;

图像高度
~~~~~~~~~~

.. code:: java

    public int height;

深度图类型
~~~~~~~~~~

.. code:: java

    /**
     * MYNTCamera.DEPTH_DATA_11_BITS
     * MYNTCamera.DEPTH_DATA_8_BITS
     *
     * */
    public int depthType;

获取bitmap
~~~~~~~~~~

.. code:: java

    public Bitmap convert2Bitmap()

获取距离（只有flag为DEPTH时，可用）
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code:: java

    public int getDistanceValue(int index)

获取距离（只有flag为DEPTH时，可用）
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code:: java

    public int getDistanceValue(int x, int y)