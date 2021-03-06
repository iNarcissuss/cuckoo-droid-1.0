Versión modificada de CuckooDroid para MSEG-18
=================================================
Modificaciones por William Rodriguez
    
Instalación
-----------

    git clone https://github.com/wrodriguezc/cuckoo-droid-1.0.git
    cd cuckoo-droid-1.0
    pip install -r requirements.txt 

Configuración adicional
-----------------------
Se debe modificar el archivo de configuración avd.conf. La ruta /Android/Sdk debe ser modificada de acuerdo a la ubicación del SDK de Android en su sistema.

    [avd]
    #Path to the local installation of the android emulator
    emulator_path = /home/{nombredeusuario}/Android/Sdk/emulator/emulator

    #Path to the local installation of the adb - android debug bridge utility.
    adb_path = /home/{nombreusuario}/Android/Sdk/platform-tools/adb

    #Path to the emulator machine files is located
    avd_path =  /home/{nombreusuario}/.android/avd

  



Ejecución
---------

Para ejecutar CuckooDroid

    cd cuckoo-droid-1.0
    ./cuckoo.sh

Para ejecutar la interfaz web, sin cerrar la terminal de CuckooDroid

    cd cuckoo-droid-1.0
    ./cuckoo-web.sh

![Image of cuckoo-droid](https://github.com/idanr1986/cuckoo-droid/blob/master/documentation/book/src/_images/logo/cuckoo.png?raw=true)

[![Black Hat Arsenal](https://www.toolswatch.org/badges/arsenal/2015.svg)]( https://www.blackhat.com/us-15/arsenal.html)
[![Black Hat Arsenal](https://www.toolswatch.org/badges/arsenal/2016.svg)]( https://www.blackhat.com/us-16/arsenal.html)

CuckooDroid - Automated Android Malware Analysis.
=================================================
Contributed By Check Point Software Technologies LTD.

CuckooDroid is an extension of Cuckoo Sandbox the Open Source software for automating analysis of suspicious files, CuckooDroid brigs to cuckoo the capabilities of execution and analysis of android application.

Installation - Easy integration script:

    git config --global user.email "you@example.com"
    git config --global user.name "Your Name"
    git clone --depth=1 https://github.com/cuckoobox/cuckoo.git cuckoo -b 1.2
    cd cuckoo
    git remote add droid https://github.com/idanr1986/cuckoo-droid
    git pull --allow-unrelated-histories --no-edit -s recursive -X theirs droid master 
    cat conf-extra/processing.conf >> conf/processing.conf
    cat conf-extra/reporting.conf >> conf/reporting.conf
    rm -r conf-extra
    echo "protobuf" >> requirements.txt

Documentation
=============
- CuckooDroid - http://cuckoo-droid.readthedocs.org/
- Cuckoo Sandbox - http://cuckoo.readthedocs.org/

You are advised to read the Cuckoo Sandbox documentation before using CuckooDroid!

Powered by:
===========
- Androguard -> https://code.google.com/p/androguard/
- Google Play Unofficial Python API -> https://github.com/egirault/googleplay-api

Credit
======
- botherder for linux_analyzer_dev -> https://github.com/cuckoobox/cuckoo/tree/linux_analyzer_dev

Authors
=======
- Idan Revivo - idanr1986@gmail.com (twitter: idanr86)
- Ofer Caspi oferc@checkpoint.com (twitter: @shablolForce)
