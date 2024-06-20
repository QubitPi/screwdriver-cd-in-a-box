Screwdriver in a Box
====================

[![GitHub Workflow Status][GitHub Workflow Status]](https://github.com/QubitPi/screwdriver-cd-in-a-box/actions/workflows/ci-cd.yml)
![Last Commit](https://img.shields.io/github/last-commit/QubitPi/screwdriver-cd-in-a-box/master?logo=github&style=for-the-badge)
[![License Badge]](./LICENSE)

This handy feature will bring up an entire Screwdriver instance (UI, API, and log store) locally for us to play with. 
All data written to a database will be stored in `data` directory.

Quickstart
----------

Requires:

- Python 3.7+
- [Docker]
- [Docker Compose v2]

1. [Login to Docker](https://docs.docker.com/engine/reference/commandline/login) with your Docker username (not
   email) or install [Docker Desktop]
2. Run the command below in the terminal to bring up a Screwdriver cluster locally.

   ```bash
   docker pull node:18
   docker pull buildpack-deps:22.04-scm

   git clone https://github.com/QubitPi/screwdriver-cd-in-a-box.git
   cd screwdriver-cd-in-a-box
   python3 setup.py
   ```

3. You will be prompted to enter your desired SCM provider as well as the Client ID and Client Secret. Afterwards, type
   `y` to launch Screwdriver!

Documentation
-------------

- [screwdriver-cd-in-a-box](https://qubitpi.github.io/screwdriver-cd-guide/cluster-management/running-locally)
- [Cluster setup](https://qubitpi.github.io/screwdriver-cd-guide/cluster-management/kubernetes) (not in-a-box anymore)

[Docker]: https://github.com/QubitPi/docker-install
[Docker Compose v2]: https://stackoverflow.com/a/66516826/14312712
[Docker Desktop]: https://www.docker.com/products/docker-desktop/

[GitHub Workflow Status]: https://img.shields.io/github/actions/workflow/status/QubitPi/screwdriver-cd-in-a-box/ci-cd.yml?branch=master&logo=github&style=for-the-badge

[License Badge]: https://img.shields.io/badge/license-BSD%203--Clause-blue.svg?style=for-the-badge
