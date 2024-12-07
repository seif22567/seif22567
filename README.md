import numpy as np
x= np.arange(1,1001)
y=x*2
print(x)
print(y)

import tensorflow as tf
model= tf.keras.layers.Sequential([
tf.keras.layers.Dense(1, input_shape=(1,),activation='Linear'),
tf.keras.layers.Dense(10),
tf.keras.layers.Dense(10),
tf.keras.layers.Dense(1)
])
model.compile(optimizer='adam', loss='mse')
model.fit(x,y, epochs=200)
model.predict(np.array([500]))
