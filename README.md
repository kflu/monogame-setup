

# Requirement on Mac

Monogame on Mac has a bug (as of 1/12/2020) where libfreeimage.dylib is not
found during build. To fix this, do the following:

```
brew install freeimage

# find the installed `libfreeimage.dylib`:
brew ls freeimage | grep -e 'libfreeimage\..*\.dylib'

# link it into the MG builder build tool folder:
ln -s \
  /usr/local/Cellar/freeimage/3.18.0/lib/libfreeimage.3.18.0.dylib \
  ~/.nuget/packages/monogame.content.builder/3.7.0.4/build/MGCB/build/libfreeimage.dylib
```
