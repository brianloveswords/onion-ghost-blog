# onion-ghost-setup

Set up secret [Ghost](https://ghost.org/) blog on the [Tor network](https://www.torproject.org/) in under a two minutes.

## Usage


1. Use [Digital Ocean](https://cloud.digitalocean.com/droplets/new) to spin up a new server pre-imaged with Ghost
![screenshot](https://cldup.com/cP-Ph2Xhh4.png)

2. Note your IP address, e.g.:
![screenshot](https://cldup.com/72AYhOBzsz.png)


3. Clone this repository
```bash
$ git clone https://github.com/brianloveswords/onion-ghost-setup.git && cd onion-ghost-setup
```

4. Run the ansible command

```bash
$ # Notice the trailing comma, that is not a typo
$ ansible-playbook provision.yml -i <your_ip_here>,
```

5. 👻 The last line of the ansible output will have your Onion hostname. 👻
![screenshot](https://cldup.com/_pegX68UuB.png)
