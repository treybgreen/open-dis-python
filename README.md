## open-dis-python

A Python 3 implementation of the Distributed Interactive Simulation (DIS) 7 standard.
Initially generated by [xmlpg](https://github.com/open-dis/xmlpg).

## Installation

First, install the dis library using:

```bash
sudo python3 setup.py install
```

or to install to your personal python installation area:

```bash
python3 setup.py install --user
```

## Running

First install application dependencies.

```bash
pip install -r requirements.txt
```

Run a receiver:

```bash
cd dis_network_example 
python3 dis_receiver.py
```

In another terminal, run the sender:

```bash
python3 dis_udp.py
```

You should also see the traffic on the net in Wireshark on your localhost interface.

Press `Ctrl+\` to stop the process.

### Git Submodules

This uses a git submodule to hold a XML description of they protocol messages. If
you regenerate the source code (you probably shouldn't) make sure the submodule
is loaded with

```
$ git submodule init
$ git submodule update
```
