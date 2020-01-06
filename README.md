# Ansible Test Lab Environment

This is a very simple testing environment for learning about [Ansible](https://www.ansible.com/) using the blog article [https://marioyepes.com/posts/ansible-introduction-for-developers/](https://marioyepes.com/posts/ansible-introduction-for-developers/)


## Setup

If you want to follow along the article with this repo, you should:


### 1. Install required software

For this test lab (not for real usage) you need the following:

- [Vagrant](https://www.vagrantup.com/) and [Virtual Box](https://www.virtualbox.org/) for the virtual machine creation
- [Homebrew](https://brew.sh/) if you are using a Mac


### 2. Clone the testlab repo

```bash
git clone https://github.com/marioy47/ansible-testlab.git
cd ansible-testlab
```

### 3. Add the new virtual hosts to `/etc/hosts`

Next you should add aliases to the _client_ hosts in your `/etc/hosts` file (on Windows 10 it's `C:\Windows\System32\drivers\etc\hosts`)

```bash
sudo vim /etc/hosts
```

And add the next 2 lines:

```txt
192.168.33.101 client1
192.168.33.102 client2
```

### 4. Initialize

And lastly you should initialize the virtual machines provided in the dirs `client1` and `client2`

```bash
cd client1
vagrant up
cd ../client2
vagrant up
```

