# Boilerplate ML
Boilerplate Python Project For Machine Learning.

# Configuration
- Need to have python 3.8+

### Creating a Python Environment
Create an empty virtual environment.
```bash
python -m venv env
```

Create a virtual environment which has included all global packages.
This option may save your data usage.
```bash
python -m venv --system-site-packages env
```


### Activating the Environment
> Recommand to use powershell on windows

```bash
source ./env/bin/activate # for linux
./env/bin/activate.bat    # for windows
```

### Install Requirements : Basic
Install Required Packages,
```bash
pip install -r requirements.txt
```

included packages in 'requirements.txt',
  - numpy==1.19.4
  - scipy==1.5.4
  - pillow==8.0.1
  - h3py==1.0.0
  - matplotlib==3.3.3
  - jupyterlab==2.2.9
  - scikit-learn==0.23.2

### Install Requirements : TensorFlow
Tensorflow package is about 300MB. It can be installed (Online),
```bash
pip install tensorflow
```

Since tensorflow package is large. It is better to download the wheel file and install it offline.
  - [Tensorflow 2.3.1 Linux (305.6 MB) DMS](https://dms.uom.lk/s/ZoeSHJwXn5MCCKc)
  - [Tensorflow 2.3.1 Windows (326.7 MB) DMS](https://dms.uom.lk/s/ejQtnik242HjnDw)

After downloading the wheel file (.whl), Tensorflow package can be installed (Offline),
```bash
pip install <path to the .whl file>
```

> Keras Comes with builtin to Tensorflow no need install or configuration

### Install Requirements : Keras
```bash
pip install keras
```

### Setup Keras Configuration
First run following code in python shell
```python
import keras
```
This will generate the keras configuration file `~/.keras/keras.json`. Its need to be looking like this,
```json
{
    "floatx": "float32",
    "epsilon": 1e-07,
    "backend": "tensorflow",
    "image_data_format": "channels_last"
}
```
to working with Keras + Tensorflow.

### Open JupyterLab inside the VE
```bash
python -m jupyterlab
```

### Exit from Virtual Environment
```bash
deactivate
```
