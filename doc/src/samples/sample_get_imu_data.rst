获取IMU数据
======================

设置IMU数据回调
~~~~~~~~~~~~~~~~

.. code:: kotlin

        mCamera?.setImuCallback { data ->

            if (data.flag == ImuData.ACCELEROMETER) {
                runOnUiThread {
                    accTextView.text = String.format("acc: x -> %.2f, y -> %.2f, z -> %.2f, timestamp -> %d, temperature -> %.2f", data.value[0], data.value[1], data.value[2], data.timestamp, data.temperature)
                }
            }
            if (data.flag == ImuData.GYROSCOPE) {
                runOnUiThread {
                    gyroTextView.text = String.format("gyro: x -> %.2f, y -> %.2f, z -> %.2f, timestamp -> %d, temperature -> %.2f", data.value[0], data.value[1], data.value[2], data.timestamp, data.temperature)
                }
            }
        }