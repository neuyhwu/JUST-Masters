# 🤖 机器学习 - 深度学习基础

深度学习在复杂模式识别中表现出色。

## 🎯 核心概念

### 1. 神经网络基础
- 感知器和激活函数
- 反向传播算法
- 优化算法（SGD、Adam）

### 2. 主流框架
```python
# TensorFlow/Keras
from tensorflow import keras

model = keras.Sequential([
    keras.layers.Dense(64, activation='relu'),
    keras.layers.Dense(32, activation='relu'),
    keras.layers.Dense(10, activation='softmax')
])

model.compile(optimizer='adam', loss='categorical_crossentropy')
model.fit(X_train, y_train, epochs=10)
```

### 3. CNN和RNN
- 卷积神经网络
- 循环神经网络
- 长短期记忆（LSTM）

---

**推荐：** 结合实际项目进行深度学习实践！
