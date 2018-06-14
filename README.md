# dragonboardBlueToothServer
1. Add java jdk 8. Note that version 10 will not work

   ```
   sudo add-apt-repository ppa:openjdk-r/ppa
   ```
   
2. Update the system package cache and install:

   ```
   sudo apt-get update
   sudo apt-get install openjdk-8-jdk
   ```
   
 3. If you have more than one Java version installed on your system use the following command to switch versions:
 
    ```
    sudo update-alternatives --config java
    ```
 4. Make sure your system is using the correct JDK:
 
    ```
    java -version
    ```
    Should say 1.8
    
 5. If you have more than one Java version installed on your system use the following command to switch versions:
 
    ```
    sudo update-alternatives --config javc
    ```
 6. Make sure you have the correct version for the javac command:
   
    ```
    javac -version
    ```
 7. Now build the tinyB.jar file. Change to the /projects directory. Create it if you do not have one.
 
    ```
    cd /projects
    mkdir tinyB
    cd tinyB
    apt-get install pkg-config
    apt-get install cmake
    apt-get install libglib2.0-dev
    apt-get install openjdk-10-jdk

    git clone https://github.com/intel-iot-devkit/tinyb.git
    cd tinyb
    mkdir build
    cd build
    cmake .. -DBUILDJAVA=ON
    make
    make install
