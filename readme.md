## Canonical Objaverse Dataset Tools
This project provides an Objaverse-related toolkit, including downloading Objaverse data, converting glb to obj files, loading canonical poses, etc

```
# Project Structure
├── Example
│   ├── load_canonicalData.py # A pipeline that includes downloads, format conversion, and canonicalization
├── Src
│   ├── DataDownload
│   │   ├── Download.py # Download Objaverse Data from internet
│   │   └── ..
│   ├── Glb2Obj
│   │   ├── glb2Obj.py  # Convert GLB files to OBJ format
│   │   └── ..
│   └── Obj2Canonicalization
│   │   ├── canon_obj.py  # Load canonical labels on object canonicalization
│   │   └── ..
│   └── structure
│   │   ├── ..
│   └── utils
│   │   ├── ..
├── data
    ├── CanonicalObjaverseDataset.json  # Canonicalization labels
    └── canon-annotations.json # Category and object's UID
```

### Requirements
The code has been tested with
- python 3.10
- pytorch 1.9.0
- pytorch3d 0.7.5
- open3d 0.14.1


### Data Processing
To test the model, please run:

```
python -m Examples.load_canonicalData --data_name 'test' 
```

To get all the COD datasets, please run:

```
python -m Examples.load_canonicalData --data_name 'canon' 
```

### License
Our code is released under MIT License (see LICENSE file for details).
