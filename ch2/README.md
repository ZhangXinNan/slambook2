
```bash
rm -rf build

mkdir build && cd build

#cmake ..
cmake ..  -DCMAKE_POLICY_VERSION_MINIMUM=3.5

make

./useHello
#Hello SLAM

./helloSLAM
#Damn, boy!
```

