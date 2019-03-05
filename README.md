# rpi_tf
Tensorflow Ver1.3 compiled whl for Raspberry Pi


# You can install Tensorflow Ver1.3.1 on your Raspberry Pi as follows
# This is based on Pyton version 2.7
git clone https://github.com/syhuh/rpi_tf.git

cd rpi_tf
cat rpi.tar* | tar xvf -

mkvirtualenv tf -p python2

workon tf

pip freeze 

pip install tensorflow-1.13.1-cp27-none-linux_armv7l.whl 
(You don't need to install numpy etc. before this action)

pip freeze
(Check packages which has a dependency to tf are installed)

pip install Pillow

cd ~/.virtualenvs/tf/lib/python2.7/site-packages
ln -s /usr/local/lib/python2.7/site-packages/cv2.so cv2.so
(If you don't have a compiled cv2, refer https://www.pyimagesearch.com/2016/04/18/install-guide-raspberry-pi-3-raspbian-jessie-opencv-3/ )

pip install matplotlib
