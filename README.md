<div id="top"></div>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->

<p align="center">
	<a href="https://github.com/silvertoken/piKube/graphs/contributors">
    	<img src="https://shields.io/github/contributors/silvertoken/piKube.svg?style=plastic" alt="Contributors">
	</a>
	<a href="https://github.com/silvertoken/piKube/network/members">
    	<img src="https://shields.io/github/forks/silvertoken/piKube.svg?style=plastic" alt="Forks">
	</a>
	<a href="https://github.com/silvertoken/piKube/stargazers">
    	<img src="https://shields.io/github/stars/silvertoken/piKube.svg?style=plastic" alt="Stars">
	</a>
	<a href="https://github.com/silvertoken/piKube/pulse">
    	<img src="https://shields.io/github/commit-activity/m/silvertoken/piKube.svg?style=plastic" alt="Commits">
	</a>
	<a href="https://github.com/silvertoken/piKube/issues">
    	<img src="https://shields.io/github/issues/silvertoken/piKube.svg?style=plastic" alt="Issues">
	</a>
	<a href="https://github.com/silvertoken/piKube/blob/master/LICENSE">
    	<img src="https://shields.io/github/license/silvertoken/piKube.svg?style=plastic" alt="License">
	</a>
</p>

<!-- PROJECT LOGO -->
<br />
<div align="center">

  <h3 align="center">piKube</h3>

  <p align="center">
    piKube is my deployment of MicroK8s on a Raspberry Pi cluster that I use for my home
    <br />
    <br />
	<a href="https://github.com/silvertoken/piKube/wiki"><strong>Read the Wiki</strong></a>
	·
    <a href="https://github.com/silvertoken/piKube/issues">Report Bugs</a>
    ·
    <a href="https://github.com/silvertoken/piKube/issues">Request Feature</a>
  </p>
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-piKube">About piKube</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>

<!-- ABOUT piKube -->
## About piKube

I built a Raspberry Pi cluster to run all my security camera's and home automation services on 5 devices.  It started to become a little tedious to update and deploy new versions as needed.  I decided it would be best to automate the build since we all know our time is precious.

My Setup:
* 5 Raspberry Pi 4's
* Mikrotik RouterBOARD 3011UiAS
* Private IP space 10.0.0.0/8
* 10.10.10.0/23 assigned to infrastructre and Metal LB

<p align="right">(<a href="#top">back to top</a>)</p>

### Built With

* [Ansible](https://www.ansible.com)
* [Python](https://www.python.org/)
* [MikroK8s](https://microk8s.io/)
* [Python](https://www.raspberrypi.org/)
* [Ubuntu](https://ubuntu.com/download/raspberry-pi)

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- GETTING STARTED -->
## Getting Started

Follow the steps listed to prepare a Raspberry Pi cluster for snap installation.  Make sure you complete the steps to enable cgroup memory listed and setup SSH keys so ansible can access each device.

* [MicroK8s Raspberry Pi Tutorial](hhttps://ubuntu.com/tutorials/how-to-kubernetes-cluster-on-raspberry-pi#1-overview)

### Prerequisites

* Ubuntu servers to install MicroK8s
* Python with virtual environments and pip

### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/silvertoken/piKube.git
   ```
3. Setup virtual environment and install requirements
   ```sh
   cd piKube
   python -m venv .venv
   source ./venv/bin/activate
   python -m pip install -r requirements.txt
   ```
4. Setup inventory file from example.yml
   
5. Run the deploy_piKube.yml against the inventory file
   ```sh
   ansible-playbook -i inventory/example.yml deploy_piKube.yml
   ```

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- USAGE EXAMPLES -->
## Usage

Use this space to show useful examples of how a project can be used. Additional screenshots, code examples and demos work well in this space. You may also link to more resources.

_For more examples, please refer to the [Documentation](https://github.com/silvertoken/hermes/wiki)_

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- CONTACT -->
## Contact

silvertoken - [@silvertoken](https://github.com/silvertoken)

Project Link: [https://github.com/silvertoken/piKube](https://github.com/silvertoken/piKube)

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://shields.io/github/contributors/silvertoken/piKube.svg?style=plastic
[contributors-url]: https://github.com/silvertoken/piKube/graphs/contributors
[forks-shield]: https://shields.io/github/forks/silvertoken/piKube.svg?style=plastic
[forks-url]: https://github.com/silvertoken/piKube/network/members
[stars-shield]: https://shields.io/github/stars/silvertoken/piKube.svg?style=plastic
[stars-url]: https://github.com/silvertoken/piKube/stargazers
[issues-shield]: https://shields.io/github/issues/silvertoken/piKube.svg?style=plastic
[issues-url]: https://github.com/silvertoken/piKube/issues
[license-shield]: https://shields.io/github/license/silvertoken/piKube.svg?style=plastic
[license-url]: https://github.com/silvertoken/piKube/blob/master/LICENSE.txt
[commits-shield]: https://shields.io/github/commit-activity/m/silvertoken/piKube.svg?style=plastic
[commits-url]: hhttps://github.com/silvertoken/piKube/pulse