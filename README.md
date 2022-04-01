# PyORB

This repository exposes to Python Uniform ORB feature point extraction.

---

## Getting Started

Wheels for Linux can be install using pip:
```bash
pip install pyorbfeature
```

### Building from source

CPP OpenCV3 and Eigen3 should be installed as a library first. If not please install first. Then clone the repository
and its submodules:

```
git clone --recursive https://github.com/LiXin97/pyorb.git
```

And finally build PyORB:

```bash
cd pyorb
pip install .
```

## Extractor uniform ORB feature

We can extractor orb feature from img path. featrue sorting as x, y, response

```python
import pyorb
import numpy as np
import cv2

img = cv2.imread({YOUR_IMG_PATH_STR_HERE})
result = pyorb.extract_frompath({YOUR_IMG_PATH_STR_HERE})
result = pyorb.extract(img)
feature = np.array(result['KeyPoints'])

print(feature.shape)
```

