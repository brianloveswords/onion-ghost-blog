# onion-ghost-blog

Set up secret [Ghost](https://ghost.org/) blog on the [Tor network](https://www.torproject.org/) in under a two minutes.

## What?

This uses ansible (a piece of software specifically for provisioning servers) to configure a Digital Ocean Ghost image for use on the Tor network.

This is based on a the [I Will Follow You into The Dark[net]presentation](http://fu.io/followdarknet) given at [Radical Networks 2015](http://radicalnetworks.org/) by [@carolinesinders](http://twitter.com/@carolinesinders), [@corcra](http://twitter.com/@corcra), and [@huertanix](http://twitter.com/@huertanix).

## Usage


1. Install [`ansible`](https://docs.ansible.com/ansible/intro_installation.html). On OS X,

   ```bash
   $ brew install ansible
   ```

   For other operating systems follow the instructions listed above.

1. Use [Digital Ocean](https://cloud.digitalocean.com/droplets/new) to spin up a new server pre-imaged with Ghost
   ![screenshot](https://cldup.com/cP-Ph2Xhh4.png)

1. Figure out the server IP address. You can get it from the [droplet list page](https://cloud.digitalocean.com/droplets)
   ![screenshot](https://cldup.com/72AYhOBzsz.png)


1. Clone this repository
   ```bash
   $ git clone https://github.com/brianloveswords/onion-ghost-blog.git && cd onion-ghost-blog
   ```

1. Run the ansible command

   ```bash
   # Notice the trailing comma, that is not a typo
   $ ansible-playbook provision.yml -i <your_ip_here>,
   ```

1. 👻 The last line of the ansible output will have your Onion hostname. 👻
   ![screenshot](https://cldup.com/_pegX68UuB.png)
