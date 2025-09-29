# RoboCupJunior CMS 2025

### Competition Management System

#### (former Rescue Scoring System)

This is a Competition Management System used in RoboCupJunior's rescue line & maze competitions worldwide.
Please refer to the [English version README](https://github.com/rrrobo/rcj-rescue-scoring-japan/blob/master/README-EN.md) for details.

---

### Competition Management System (CMS)

#### (formerly: Rescue Scoring System)

This is a competition management system used in RoboCupJunior rescue competitions.

#### Supported Rules

* 2024 Rules issued by the International RoboCupJunior Rescue Committee
* Rescue Line Entry 2024 Rules issued by the Japan Rescue Technical Committee

---

This project is developed as a fork from the [original project](https://github.com/TechnoX/rcj-rescue-scoring).
Main changes include:

* Enhanced user management functions
* Added map rotation function
* Added interview functionality
* Support for International 2024 rules
* Support for tile set inventory management in Line competitions
* Support for backup/restore of competition data
* Support for handover in case of trouble
* Support for printing paper score sheets
* Integrated document submission/review system
* Email distribution from the system
* Support for Rescue Line Entry / Rescue Maze Entry 2023 rules

Unless there is a special reason, it is recommended to use the version provided in this repository.

---

## Live Demo

The latest version is running. It is built on an OCI ARM instance using a Docker image.

[https://osaka.rcj.cloud](https://osaka.rcj.cloud)

---

## Update History

* [2023/06/04] Supported International 2023 rules
* [2022/10/09] Supported Rescue Maze Entry 2023 rules
* [2022/09/17] Supported Rescue Line Entry 2023 rules
* [2021/10/02] Tentative support for 2022 rules
* [2021/03/07] Official support for 2021 rules
* [2020/11/28] Integrated document system into this system; enabled email distribution to teams
* [2020/02/10] v20 series supports 2020 rules
* [2019/07/17] Score sheet output enabled
* [2019/03/19] Competition data backup enabled; major UI changes on the top page
* [2018/10/24] v19 series supports 2019 rules; backward compatible with 2018 rules

---

## Usage Record

A list of major competitions where this system has been used (**as far as known**). Includes derived versions.

### 2016 Rules Version

* Sweden National Competition
* RoboCupJunior 2017 Kanto Block Competition
* RoboCupJunior Japan Open 2017 Gifu/Nakatsugawa

### 2017 Rules Version

* RoboCup 2017 Nagoya Japan
* NEST Robocon 2017
* RoboCupJunior 2018 North Saitama Node Competition
* RoboCupJunior 2018 South Saitama Node Competition
* RoboCupJunior 2018 Chiba Node Competition
* RoboCupJunior 2018 Hiroshima Node Competition
* RoboCupJunior 2018 Osaka Central Node Competition
* RoboCupJunior 2018 Saitama Block Competition
* RoboCupJunior 2018 Kanto Block Competition
* RoboCupJunior 2018 Hiroshima Block Competition
* RoboCupJunior 2018 Kansai Block Competition
* RoboCupJunior Japan Open 2018 Wakayama

### 2018 Rules Version

* RoboCup 2018 Montreal Canada
* Kansai Block Summer Open Competition 2018

### 2019 Rules Version

* RoboCupJunior 2019 Tokai Block Competition
* RoboCupJunior 2019 Saitama Block Competition
* RoboCupJunior 2019 Hiroshima Block Competition
* RoboCupJunior 2019 Osaka Central Node Competition
* RoboCupJunior 2019 Kansai Block Competition
* RoboCupJunior 2019 Kanto Block Competition
* RoboCupJunior Japan Open 2019 Wakayama
* RoboCup 2019 Sydney Australia
* RoboCupJunior 2020 Osaka Central Node Competition
* RoboCupJunior 2020 Kansai Block Competition

### 2021 Rules Version

* RoboCupJunior 2021 Tokai Block Competition
* RoboCupJunior Japan Open 2021 Online
* RoboCup 2021 Worldwide

### 2022 Rules Version

* RoboCup 2022 Bangkok Thailand

### 2023 Rules Version

* RoboCupJunior 2023 Tokai Block Competition
* RoboCupJunior 2023 Kanto Block Competition
* RoboCupJunior 2023 Kansai Block Competition
* RoboCupJunior 2023 Hiroshima Block Competition
* RoboCupJunior Japan Open 2023 Nagoya
* Torneo Mexicano de Robótica 2023 (Mexico)
* RoboCup 2023 Bordeaux France

### 2024 Rules Version

* RoboCup Junior Japan Open 2024 Nagoya
* RoboCup 2024 Eindhoven

---

## Usage

### Using Docker (Recommended)

[Official Docker Image](https://hub.docker.com/repository/docker/ryorobo/rcj-cms) is available. Usage of this image is recommended.
The official Docker image supports the following architectures:

* linux/amd64
* linux/arm/v6
* linux/arm/v7
* linux/arm64

A helper file for environment setup is also provided: [Helper Repository](https://github.com/rrrobo/rcj-cms-docker-helper).

### Without Docker

#### Required Software

* [Node.js](https://nodejs.org/en/)
* [MongoDB](https://www.mongodb.com)

Install these two first.

#### Install bower

```bash
sudo npm install -g bower
```

#### Install dependencies

In the project directory:

```bash
npm install
bower install
npm run build
```

#### Create log directory

```bash
mkdir logs
```

#### Create documents directory

```bash
mkdir documents
```

#### Start the server

```bash
node server
```

---

## Initial Account

The default initial account is:

| Username | Password  |
| -------- | --------- |
| admin    | adminpass |

---

## Email Settings

To send emails from the system, configure your SMTP server information.
Add the following to `process.env`. Adjust to your environment; copy-pasting will not work as-is.

```
MAIL_SMTP=smtp.example.com
MAIL_PORT=587
MAIL_USER=smtp_user
MAIL_PASS=smtp_password
MAIL_FROM=fromAddress@example.com
MAIL_SENDER=RoboCupJunior Japan
```

---

## More Information

See the [RCJ Scoring System Community Forum](https://ask.rcj.cloud).
Currently, access to this forum is limited to local competition organizers.
If you wish to access, please contact your regional Rescue Technical Committee.

---

## Example Screenshots

(*Includes information from older versions*)

Top Page (2019) <img src="https://raw.githubusercontent.com/rrrobo/rcj-rescue-scoring-japan/master/rcjj-scoring/1.png">

<hr>
Login Page  
<img src="https://raw.githubusercontent.com/rrrobo/rcj-rescue-scoring-japan/master/rcjj-scoring/6.png">
<hr>
Line Competition List  
<img src="https://raw.githubusercontent.com/rrrobo/rcj-rescue-scoring-japan/master/rcjj-scoring/2.png">
<hr>
Line Judge 1  
<img src="https://raw.githubusercontent.com/rrrobo/rcj-rescue-scoring-japan/master/rcjj-scoring/3.png">
<hr>
Line Judge 2  
<img src="https://raw.githubusercontent.com/rrrobo/rcj-rescue-scoring-japan/master/rcjj-scoring/4.png">
<hr>
Line Confirmation  
<img src="https://raw.githubusercontent.com/rrrobo/rcj-rescue-scoring-japan/master/rcjj-scoring/5.png">
