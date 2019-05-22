---
layout: default
title: Installation
nav_order: 99
---

# Installation and Usage
{: .no_toc }


This page provides the instructions on installing and running <span style="font-variant:small-caps;">GoalExplorer</span>.
{: .fs-6 .fw-300 }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Getting started

### Prerequisites

Java Runtime Environment version 8 or later is required.

The static analyzer depends on Soot and FlowDroid (for modeling Android lifecycle) and IC3 (for decoding Intents):

- [Soot](https://github.com/Sable/soot) : Soot - A Java optimization framework

- [IC3](http://siis.cse.psu.edu/ic3/) : Inter-Component Communication Analysis for Android

- [FlowDroid](https://github.com/secure-software-engineering/FlowDroid/) : FlowDroid Static Data Flow Tracker

The dynamic explorer is built on top of [Stoat](https://github.com/tingsu/Stoat), and it depends on Python, Ruby, Nokogiri, and UiAutomator:

- [Ruby](https://www.ruby-lang.org/en/) : 2.1

- [Python](https://www.python.org/) : 2.7

- [Nokogiri](https://nokogiri.org/tutorials/installing_nokogiri.html) : HTML, XML, SAX, and Reader parser

- [uiautomator](https://github.com/xiaocong/uiautomator) : Python wrapper of Android uiautomator test tool

### Setup

<span style="font-variant:small-caps;">GoalExplorer</span> is built using Maven. Use

```yaml
mvn install
```

The FlowDroid module contains DroidBench tests, so you may want to build the tool without the tests (over 400 tests in total), try

```yaml
mvn -DskipTests install
```
Maven should take care of all dependencies that are required for the build, and the built JAR files can be found in the "target" folder of the respective modules.

Please make sure that ic3-android.jar, AndroidCallbacks.txt and icc.cmodel are in the same directory as the JAR file, so that the inter-component communication model generated from IC3 can be used for better ICC modeling.

To setup the dynamic explorer, you need to install [Android SDK](https://developer.android.com/studio/releases/sdk-tools) and create emulators if you plan to run on emulator. See [this link](https://stackoverflow.com/questions/43275238/how-to-set-system-images-path-when-creating-an-android-avd) on how to create avd using [avdmanager](https://developer.android.com/studio/command-line/avdmanager).

The current version only supports running on emulators.

Please export ANDROID_HOME (for android sdk), PYTHON_PATH (for uiautomator), CLASSPATH (for soot)

Example:
```
export ANDROID_HOME="/home/XX/Android/Sdk"
export PYTHONPATH="/home/XX/uiautomator"
export CLASSPATH="/home/XX/fsmdroid/soot-github/lib/soot-develop.jar
export PATH=$PATH:${ANDROID_HOME}/build-tools/25.0.0:${ANDROID_HOME}/emulator:${ANDROID_HOME}/tools:${ANDROID_HOME}/tools/bin:${ANDROID_HOME}/platform-tools:
```

You may also need to modify "Stoat/CONF.txt" to set the Stoat path.

---

## Usage

### Generating GUI model of the app

First generates the static UI model of the app (STG) using the command:

```yaml
java -jar {JAR_PATH} ge [OPTIONS] [-cb <arg>] [-d] [-h] -i <arg> 
          [-l <arg>] [-o <arg>] [-s <arg>] [-t <arg>] [-v]
```

#### Available Options


```yaml
  usage: ge [OPTIONS] [-cb <arg>] [-cg <arg>] [-d] [-h] -i <arg> 
            [-l <arg>] [-o <arg>] [-s <arg>] [-t <arg>] [-v]
   -cb <arg>           the maximum number of callbacks modeled for each
                       component (default to 20)
   -d,--debug          debug mode (default disabled)
   -h,--help           print the help message
   -i,--input <arg>    input apk path (required)
   -l,--api <arg>      api level (default to 23)
   -o,--output <arg>   output directory (default to "sootOutput")
   -s,--sdk <arg>      path to android sdk (default value can be set in
                       config file)
   -t <arg>            maximum timeout during callback analysis in seconds
                       (default: 60)
   -v,--version        print version info
```

### Dynamic exploration

Run the dynamic explorer with the generated STG as the input:

```yaml
ruby run_stoat_testing.rb --app_dir /home/XX/Bites.apk --avd_name testAVD_1 
--avd_port 5554 --stoat_port 2000 --model /path/to/model
```
