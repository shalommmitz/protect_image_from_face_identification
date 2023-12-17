Starting image: pics/original.png

## Starting point

The folder named pics contains the pic original.png

## Install fawkes

pip install fawkes

Fix error:

change the file `~/.local/lib/python3.10/site-packages/fawkes/differentiator.py`
   change the line `optimizer = tf.keras.optimizers.Adadelta(float(self.learning_rate))`
   to `optimizer = tf.keras.optimizers.legacy.Adadelta(float(self.learning_rate))`

## change pics/original.png to pics/original_cloaked.png

   `fawkes --mode mid --directory pics`

## Optional: change the aspect ratio of the pic

Using pinta

## Install facemorpher

```
apt update
sudo apt install python3-opencv libopencv-dev
sudo ln -s /usr/include/opencv4/opencv2 /usr/include/
pip install facemorpher
```

# Morph the pic

Create 'fake.png' (should be similar to your real pic) using https://this-person-does-not-exist.com/en

cd pics

facemorpher  --src=original_cloaked.png --dest=fake.png --num=20 --out_frames=. --background=transparent

Now, select a picture (frame005 ?) that is not too much different.

Unite the chosen picture with the original_cloaked.png picture - and you are done.
