# Lunar Reader

*Lunar Reader for fx-9750/9860GIII, running on [C.Basic](https://cbasic.fandom.com/wiki/C.Basic_Wiki)*

> **Note** This project currently only supports GBK (Chinese) encoding, which is compatible with ASCII and can display part of Japanese, Russian, and Greek.

|Version Tag|Release Code|What's New|
|---|---|---|
|v1.5.x|X-Ray|Table of Contents|
|v1.4.x|Sunloar|Optmize UI,fix bugs|
|v1.3.x|Sophia|Low memory mode (Disabled in later version)|
|v1.2.x|Stephen|Add GPLv3 license|
|v1.0.x|Unstable|First release|

## 

## Usage

> **Note** Since this project relies on C.Basic, it may exhibit some unexpected behaviors, most of which are due to the characteristics of C.Basic or which C.Basic dose not supports. Please check carefully before submitting an issue.

### Open File

> **Note** I have tried to develop an easy-to-use UI interface for file selection, but C.Basic couldn’t list files in the directory, so they won’t appear.

Just enter file path (Use linux style `/`).

### Page Up/Down

Press <kbd>Up</kbd> or <kbd>Down</kbd> arrow key.

A gray mask will be displayed on the space after EOF, or replace unavailable character.

### Byte In/Out

Press <kbd>Left</kbd> or <kbd>Right</kbd> arrow key.

It's usefull when you're break out the double-byte GBK encoding character.

### Jump

Press <kbd>F1</kbd>. Enter hexadecimal number (<kbd>X,Theta,T</kbd> ~ <kbd>tan</kbd> for A ~ F), then press <kbd>EXE</kbd>.

### Table of Contents

Press <kbd>F4</kbd>.

When first open one file, this program will scan for it's contents, please wait for a monment.

> **Note** I've tried to use C.Basic native string search function but it dose not work as expected on GBK encoding file.

It dose scanning for `<LF>` character, then test if the next character is in `[*#-0123456789第` (the last one is a Chinese character which is a prefix means "N-th").
