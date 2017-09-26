# YMF825Board Sample Module

## About this Sample Module

This sample program is a software module for using YMF825 as a MIDI tone generator. It's available for the following MIDI Commands.
+ Key On / Key Off
+ Program Change
+ Control Change #1
+ Control Change #7
+ Control Change #64
+ Pitch Bend

## How to use on Arduino

+ Create a folder for development and copy all files in /common and files in /arduino to the folder together.
+ Open the .ino file from Arduino IDE.
+ After successfully loading, each file will appear on the tab area. If you do Verify and Upload as it is, Arduino will work.
+ ymf825board_sample2.ino is a program that automatically plays 1 octave by the semitone in order.

## How to use on Raspberry Pi

+ Since the use of the bcm2835 library is a prerequisite, install the bcm2835 library.
+ Please configure setting of makefile so that all files in /common and files in /raspi are compiled.


## Module Interface
| Function Name | details | When it's called | include file |
|---|---|---|---|
|initSPI()|initialize SPI|in a application initialize section|fmsd1.h|
|initSD1()|initialize YMF825(SD1)|in a application initialize section(after initSPI())|fmsd1.h|
|Fmdriver_init()|initialize the module|after initSD1()|fmif.h|
|Fmdriver_sendMidi()|send MIDI messages to the module|when it has gotten a MIDI message|fmif.h|

+ In the case of Arduino, please wrap '#include fmif.h' in 'extern "C"{}'.


## ���̃T���v���ɂ���

�{�T���v���v���O�����́AYMF825��MIDI���������邽�߂̃\�t�g�E�F�A���W���[���ł��B�ȉ���MIDI Command�ɑΉ����Ă��܂��B
+ Key On / Key Off
+ Program Change
+ Control Change #1
+ Control Change #7
+ Control Change #64
+ Pitch Bend

## Arduino�ł̎g����

+ �J���p�̃t�H���_�����A������ /common ���̃t�@�C���ƁA /arduino ���̃t�@�C����S�Ă��̃t�H���_�ɃR�s�[���܂��B
+ ���̏�ԂŁAArduino IDE ���� .ino �t�@�C�����J���܂��B
+ ����ɓǂݍ��߂���A�e�t�@�C�����^�u��Ɍ���܂��B���̂܂܌��؂Ə������݂��s���΁AArduino�����삵�܂��B
+ ymf825board_sample2.ino �͔����P�ʂ�1octave�������ɔ�������v���O�����ł��B


## Raspberry Pi�ł̎g����

+ bcm2835���C�u�����̎g�p���O��ƂȂ��Ă��܂��̂ŁAbcm2835���C�u�������C���X�g�[�����Ă��������B
+ /common ���̃t�@�C���ƁA/raspi ���̃t�@�C�����S���R���p�C�������悤�ɁAmakefile�̐ݒ���s���Ă��������B


## Module Interface
| �֐��� | �������e | �R�[������^�C�~���O | include file |
|---|---|---|---|
|initSPI()|SPI�̏�����|�A�v���̏���������|fmsd1.h|
|initSD1()|YMF825(SD1)�̏�����|�A�v���̏���������(initSPI()�̌�)|fmsd1.h|
|Fmdriver_init()|���̃��W���[���̏�����|initSD1()�̌�|fmif.h|
|Fmdriver_sendMidi()|���̃��W���[����MIDI�𑗂�|MIDI���b�Z�[�W��M��|fmif.h|

+ Arduino�Ŏg�p����ꍇ '#include fmif.h' �� 'extern "C"{}'�ň͂�ł��������B


