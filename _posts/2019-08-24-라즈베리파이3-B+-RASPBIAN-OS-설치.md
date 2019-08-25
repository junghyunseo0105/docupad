---
title: "라즈베리파이3 B+ RASPBIAN OS 설치"
layout: single
category: raspberry
toc: true
toc_label: "목차"
toc_icon: "cog"
---

## 준비

Raspberry 를 다루기 전에 꼭 준비해야 될 것을 알려드리 겠습니다. Raspberry 를 처음 다루신다면 키트를 구매하여 실습을 하시는 것이 좋습니다.
왜냐하면 Raspberry 를 구매하고 나면 필요한 준비물들이 하나 씩 생기기 때문에 추가 물품을 준비하느라 번거로움이 생깁니다. 밑의 리스트는 Raspberry 를 구동을 위한 리스트입니다.

* Raspberry 3 B+
* 2.5A 이상 충전기
* micro sd card
* micro sd card 리더기
* 키보드, 마우스, HDMI 모니터

## 다운 및 설치 프로그램
* [라즈비안 OS 설치 사이트 접속하기]에 접속하여 [Raspbian Buster with desktop] 를 ZIP 파일로 다운로드 합니다.
* [balenaEtcher 설치 사이트 접속하기]에 접속하여 자신의 컴퓨터에 맞게 설치하여 줍니다.

## 라즈비안 OS
* Raspbian Buster with desktop 이란? 
   * GUI 가 있는 버전으로 일반적으로 윈도우 10과 비슷한 환경을 만들어 줍니다.
* Raspbian Buster Lite 이란?
   * GUI 가 없는 버전으로 오직 리눅스 명령어로만 사용가능합니다.

## balenaEtcher
* 라즈비안 OS를 micro SD에 굽기 위해 사용되는 프로그램입니다.

[라즈비안 OS 설치 사이트 접속하기]: https://www.raspberrypi.org/downloads/raspbian/
[balenaEtcher 설치 사이트 접속하기]: https://www.balena.io/etcher/

## 라즈베리파이 세팅
* 라즈베리파이에 2.5A 이상의 전원, HDMI가 지원되는 모니터, 마우스, 키보드를 연결합니다.
* microSD 카드 리더기에 microSD 카드를 꽂은 후 컴퓨터에 연결하여 줍니다.

## 라즈비안 OS 굽기
* balenaEtcher 를 실행하여 [Selection Image] 를 클릭하여 ZIP을 선택하여 줍니다.
* 모든 작업이 끝날 시 자동으로 해제가 되니 그대로 뽑아 라즈베리파이에 넣어줍니다.

## 라즈베리파이 실행
* 전원을 넣어주면 자동으로 OS가 설치됩니다.
