This is a fork from the numerical weather prediction course @36c3. The original can be found here: https://git.hacknology.de/projekte/wrftut

# NWP/WRF tutorial

Contact: [tecer](mailto:tecer@hacknology.de)

## Preparation

In order to get a virtual machine up and running, install [VirtualBox](https://www.virtualbox.org/) and [Vagrant](https://vagrantup.com/) (available for many operating systems).
Alternatively (but EXPERIMENTAL - note the WRF+OpenMPI does not properly work with Docker): [Docker](https://www.docker.com) and [Vagrant](https://vagrantup.com/).

Clone this repository
```bash
> git clone https://git.hacknology.de/projekte/wrftut.git
```

### Virtualbox

Then
```bash
> cd wrftut
wrftut> vagrant up
```

This downloads and starts the prepared virtual machine image (~2GB).
The virtual machine can either used directly, or via ssh:
```bash
wrftut> vagrant ssh
```

### Docker Vagrantbox (EXPERIMENTAL)

Alternatively, try the Docker Vagrantbox via
```bash
> cd wrftut
> cp Vagrantfile Vagrantfile-vbox
> cp Vegrantfile-docker Vagrantfile
> vagrant up
> vagrant ssh
```
(you may need to enter the password for box user `vagrant`, which is `vagrant`)

### Docker (EXPERIMENTAL)

Alternatively, if you don't like to use Vagrant, you can try to use the Docker image directly.
```bash
> docker pull tcriess/wrftut-2019
> docker run -p 2222:22 -d tcriess/wrftut-2019
> ssh -p 2222 vagrant@127.0.0.1
```
(Username/Password for ssh is `vagrant`/`vagrant`)

## Compiling and running WRF

See presentation.

## Cheating

There are also Vagrantboxes containing all executables and all result files.
Edit the Vagrantfile to use the "-complete" Vagrantbox instead.

## Visualising the results

Programs for visualisation are best run on the host, not on the virtual machine.
We catch a short glimpse of [QGIS](https://www.qgis.org), [IDV](https://www.unidata.ucar.edu/software/idv/) and [VAPOR](https://www.vapor.ucar.edu/), so if make sure to have at least one of these installed on your laptop.

## Links

[Benni's Arch Linux repo](https://github.com/SettRaziel/wrf_archlinux)

[WeatherGlobe](http://wg.square-wave.de)

[WindSystem](http://wg.square-wave.de/index-ws.html)
