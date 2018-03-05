# OVERVIEW

qMIDASAPI is a cross-platform Qt-based library allowing to easily query a [Midas](https://github.com/midasplatform/midas) server.

---

**Update**: Girder https://github.com/girder/girder is a more modern, better supported application than Midas Server. Look at Girder before using Midas Server.

---

## Prerequisites

 * Qt 4
 * CMake

## How to build

    git clone git://github.com/finetjul/qMidasAPI.git
    mkdir qMidasAPI-build
    cd qMidasAPI-build
    cmake -DQT_QMAKE_EXECUTABLE:FILEPATH=/path/to/cmake ../qMidasAPI
    make -j4
    ctest

## Contribute
Fork + pull.
