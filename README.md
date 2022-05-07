# dC-install

## Wymagania:
* git
* bash

## Instalacja:
0. ```
ash$ cat > dc-install-prep << EOF
git
bash
EOF
```
1. `ash$ sce-import -lb dc-install-prep`
2. `ash$ sce-load dc-install-prep`
3. `ash$ bash`
4. `bash$ git clone https://github.com/xf0r3m/dC-install.git`
5. `bash$ chmod +x dC-install/dC-install.sh`

## Użycie:
  * dla dCore (Uwaga, dC-install nie za bardzo działa z dCore-trusty):
   `bash$ ./dC-install dCore <nośnik instalacji> <dysk docelowy>`
  
  * dla OTP:
    `bash$ ./dC-install OTP <nośnik instalacji> <dysk docelowy>`

Nośnik instalacji może przybierać różne nazwy w zależności od tego czy
uruchomiliśmy system z płyty (głównie dCore), czy z pendrive-a (OTP). 

### Przykład:
`bash -x ~/dC-install/dC-install.sh dCore /dev/sr0 /dev/sda 2>&1 | tee ~/dC-install/dC-install.sh.log`

### Uwagi:
Instalacja może się nie powieść, na przykład jeśli zobaczymy przy wyborze
docelowego katalogu dla rozszrzeń `/mnt/sr0`, wówczas możemy uruchmić
skrypt jeszcze raz, a drugim razem system powienien zostać poprawnie 
zainstalowany.
