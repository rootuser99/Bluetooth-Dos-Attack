# Bluetooth-Dos-Attack
## Disclaimer
<p align="center">This project was created only for good purposes and personal use.</p>

THIS SOFTWARE IS PROVIDED "AS IS" WITHOUT WARRANTY OF ANY KIND. YOU MAY USE THIS SOFTWARE AT YOUR OWN RISK. THE USE IS COMPLETE RESPONSIBILITY OF THE END-USER. THE DEVELOPERS ASSUME NO LIABILITY AND ARE NOT RESPONSIBLE FOR ANY MISUSE OR DAMAGE CAUSED BY THIS PROGRAM.

## Installing

```
$ sudo apt update
$ sudo apt install python3
$ sudo git clone https://github.com/jieggiI/BLUETOOTH-DOS-ATTACK-SCRIPT.git
$ cd BLUETOOTH-DOS-ATTACK-SCRIPT/
$ python3 Bluetooth-DOS-Attack.py

### Note
<p>The script works only with Linux systems.</p>
<p>You must have "l2ping" util on your linux machine (it installed as default on Kali Linux).</p>
<p>YOU MUST SCAN AND ATTACK BEFORE SOMEONE CONNECT TO THE TARGET!!!</p>

## Using
<p>First of all, you must scan network for Bluetooth devises. For example, you can use "hcitool".</p>

```
$ sudo apt update

$ apt install hcitool

$ sudo service bluetooth start

$ hcitool scan
```
<p>Output will be like:</p>

```
A1:B2:C3:D6:E7      Xiaomi portable speaker
B1:C2:D3:E4:F5      iPhone(Toivo)
C1:D2:E3:F4:G5      Some Bluetooth device
```
<p>Then copy target addres (for example "A1:B2:C3:D6:E7") and paste it in "Target addr".</p>


## Manual

1. "Target addr" - addres of your target (Check info above).
2. "Packages size" - size of the packages, that will be sent to the target. 600 is optimal.
3. "Threads count" - number of threads, that will send packages to the target at the same time. I used 500 threads, and that was enough. Check the table below, to find optimal value.

|  Packages size | Threads count| Ping, ms  | Distance, meters | Time waited, sec  | Device |
|:--------------:|:-----: |:------------:|:--------------------:|:----------------:|:------:|
|  600           | 1       | 9           |0,3                   |           5      |Xiaomi Mi Portable Bluetooth Speaker|
|  600           | 10      | 38          |0,3                   |           5      |Xiaomi Mi Portable Bluetooth Speaker|
|  600           | 20      | 78          |0,3                   |           5      |Xiaomi Mi Portable Bluetooth Speaker|
|  600           | 50      | 229         |0,3                   |           5      |Xiaomi Mi Portable Bluetooth Speaker|
|  600           | 100     | 413         |0,3                   |           5      |Xiaomi Mi Portable Bluetooth Speaker|
|  600           | 200     | 806         |0,3                   |           5      |Xiaomi Mi Portable Bluetooth Speaker|
|  600           | 500     | 1961        |0,3                   |           5      |Xiaomi Mi Portable Bluetooth Speaker|
|  600           | 1000    | 6621        |0,3                   |           5      |Xiaomi Mi Portable Bluetooth Speaker|
|  600           | 1000+   | Couldn't calculate  |0,3           |           5      |Xiaomi Mi Portable Bluetooth Speaker| 

<h5>I recommed too use Package size 200 And Threads 300 First(for safety).if it doesn't work then you may incrrease the package and threads as you feel compatable.</h5>

## What happens to the target device

<p>I can't say about all devices what would hppen to them.</p>
