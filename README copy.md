# staring-out-game-with-opencvの動かし方，およびバグの修正

AIにらめっこデモンストレーションMBS（M1Macのみ）
# githubからダウンロードする
git clone git@github.com:yasu-kun/staring-out-game-with-opencv.git
# 
(base) ~ $ conda env create -n face_emo -f face_emo.yml
# ディレクトリの移動
(base) $ cd staring-out-game-with-opencv 
# face_emoを起動する
(base) $ conda activate face_emo                       
# 起動すると環境が構築され，(base)が(face_emo)に変わる
(face_emo) ~ $ python predict.py    

# 画面内のカメラをずらす
(face_emo) staring-out-game-with-opencv $ conda deactivate

# 以下いろいろなエラー

エラー(4/21)
(face_emo) kai@kai staring-out-game-with-opencv % python predict.py
Traceback (most recent call last):
  File "predict.py", line 3, in <module>
    from keras.models import load_model
  File "/opt/homebrew/Caskroom/miniforge/base/envs/face_emo/lib/python3.8/site-packages/keras/__init__.py", line 21, in <module>
    from keras import models
  File "/opt/homebrew/Caskroom/miniforge/base/envs/face_emo/lib/python3.8/site-packages/keras/models/__init__.py", line 18, in <module>
    from keras.engine.functional import Functional
  File "/opt/homebrew/Caskroom/miniforge/base/envs/face_emo/lib/python3.8/site-packages/keras/engine/functional.py", line 24, in <module>
    import tensorflow.compat.v2 as tf
  File "/opt/homebrew/Caskroom/miniforge/base/envs/face_emo/lib/python3.8/site-packages/tensorflow/__init__.py", line 24, in <module>
    from tensorflow.python import pywrap_tensorflow  # pylint: disable=unused-import
  File "/opt/homebrew/Caskroom/miniforge/base/envs/face_emo/lib/python3.8/site-packages/tensorflow/python/__init__.py", line 49, in <module>
    from tensorflow.python import pywrap_tensorflow
  File "/opt/homebrew/Caskroom/miniforge/base/envs/face_emo/lib/python3.8/site-packages/tensorflow/python/pywrap_tensorflow.py", line 58, in <module>
    from tensorflow.python.pywrap_tensorflow_internal import *
  File "/opt/homebrew/Caskroom/miniforge/base/envs/face_emo/lib/python3.8/site-packages/tensorflow/python/pywrap_tensorflow_internal.py", line 114
    def TFE_ContextOptionsSetAsync(arg1, async):
                                         ^
SyntaxError: invalid syntax

（参考）
Anacondaを使った仮想環境を保存・再構築、複製
https://qiita.com/ozaki_physics/items/13466d6d1954a0afeb3b
