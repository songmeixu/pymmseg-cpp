pymmseg-cpp is a Python port of the rmmseg-cpp project. rmmseg-cpp is a MMSEG Chinese word segmenting algorithm implemented in C++ with a Ruby interface.

Download the binary release on the right sidebar and copy the `pymmseg` directory to your Python's path (e.g. `/usr/lib/python2.5/site-packages/`). Here's an example of usage:
```
from pymmseg import mmseg
 
mmseg.dict_load_defaults()
text = # ...
algor = mmseg.Algorithm(text)
for tok in algor:
    print '%s [%d..%d]' % (tok.text, tok.start, tok.end)
```

Or you can download the source tarball or check out the latest code from the git repo hosted at [github](http://github.com/pluskid/pymmseg-cpp/). Then you'll need to build the mmseg-cpp module yourself: goto the `mmseg-cpp` subdirectory and run the `build.py` script. It will build the native module for you.

For more information, refer to the [README](http://github.com/pluskid/pymmseg-cpp/tree/master/README) file.