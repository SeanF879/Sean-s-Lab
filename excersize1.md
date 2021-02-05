
##1) In the video Maroney details the way that ML is different from
# traditional programming.  In the traditional way, you create code and that code has rules that interpret data in a way to give you results
#However, in ML you have results and data to find rules.

import tensorflow as tf
import numpy as np
from tensorflow import keras

#Above imports the required libraries

model = tf.keras.Sequential([keras.layers.Dense(units=1,input_shape=[1])])


model.compile(optimizer = 'sgd', loss = 'mean_squared_error')

xs = np.array([-1.0, 0.0, 1.0, 2.0, 3.0, 4.0], dtype=float)
ys = np.array([-2.0, 1.0, 4.0, 7.0, 10.0, 13.0], dtype=float)

model.fit(xs, ys, epochs=500)
print(model.predict([7.0]))

#The above is the first result, which returns a 21.998814


model = tf.keras.Sequential([keras.layers.Dense(units=1,input_shape=[1])])


model.compile(optimizer = 'sgd', loss = 'mean_squared_error')

xs = np.array([-1.0, 0.0, 1.0, 2.0, 3.0, 4.0], dtype=float)
ys = np.array([-2.0, 1.0, 4.0, 7.0, 10.0, 13.0], dtype=float)

model.fit(xs, ys, epochs=500)
print(model.predict([7.0]))

##The above is the result from the 2nd iteration, which returns a result of 21.99073
##The results are different depending on which iteration you run because it is a machine elarning program, which means that with every iteration the model becomes optimized and learns in its own way.  So the second time was different from the first.

##Below is the code for the house price data

model_home = tf.keras.Sequential([keras.layers.Dense(units=1,input_shape=[1])])
model_home.compile(optimizer = 'sgd', loss = 'mean_squared_error')
xs_home = np.array([4.0, 3.0, 5.0, 4.0, 2.0, 3.0], dtype=float)
ys_home = np.array([4.0, 1.0, 3.5, 2.9, 2.5, 2.3], dtype=float)

model.fit(xs_home, ys_home, epochs=1000)
print(model.predict([4.0]))
#Above returns 3.00422
print(model.predict([3.0]))
#Above returns 2.3877
print(model.predict([5.0]))
#Above returns 3.620
print(model.predict([4.0]))
#Above returns 3.000
print(model.predict([2.0]))
#Above returns 1.7713
print(model.predict([3.0]))
#Above returns 2.3877

##Therefore the hugdins house is the best deal here, with a predicted price of about
#$238,770 and a actual price of less than half that
#Meanwhile the worst deal is the moon house, which has a price of about $75,000
#over the model's predicted price
