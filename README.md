# English
## mcl_with_vagrant
This repository run the vagrant image (Ubuntu 16.04) which contains requirements for running MCL mining or staking. You can look at http://marmara.io for information.

## Requirements
*   install virtual box from https://www.virtualbox.org/wiki/Downloads
*   install vagrant from https://www.vagrantup.com/downloads
*   clone this repository with `git clone https://github.com/adilkaraoz/mcl_with_vagrant.git` or download as zip and open somewhere

## Steps to start
*   Enter the repository folder you cloned or extract.
*   Change WORKER_COUNT at Vagrantfile or leave as is (according to machine count you want to run)
*   Run `vagrant up` wait for downloading box and running virtual machine
*   You can connect to virtual machine with `vagrant ssh worker01`command. Change 01 as 02, 03 etc. which virtual machine you want to connect
*   You don't have to use the komodo commands with ./, komodod and komodo-cli already added to your path. So, you can run with `komodod` directly
*   Follow the step at https://github.com/marmarachain/Marmara-v.1.0 to create or import your wallet then start mining or staking. (Skip Marmara Setup)

# Türkçe
## mcl_with_vagrant
Bu repo tüm MCL mining veya staking yapmak için gereksinimleri içeren Ubuntu 16.04 vagrant imajını içerir. Detaylı bilgiyi http://marmara.io adresinde bulabilirsiniz.

## Requirements
*   https://www.virtualbox.org/wiki/Downloads adresinden Virtual Box'ı indirin ve yükleyin.
*   https://www.vagrantup.com/downloads adresinden Vagrant'ı indirin ve yükleyin.
*   Bu repo'yu `git clone https://github.com/adilkaraoz/mcl_with_vagrant.git` komutu ile klonlayın veya zip olarak indirip bir yere ayıklayın.

## Başlamak için adımlar
*   Repo'yu indirdiğiniz veya klonladığınız yere gidip klasör içerisine girin.
*   Vagrantfile dosyasındaki WORKER_COUNT değerini ne kadar makine çalıştıracaksanız o şekilde değiştirin veya olduğu gibi bırakın.
*   `vagrant up` komutunu çalıştırın ve imajın indirilmesi ve çalıştırılmasına kadar bekleyin.
*   Sanal makineye `vagrant ssh worker01` komutu ile bağlanabilirsiniz. 01 değerini, hangi makineye bağlanacaksanız o şekilde değiştirin.
*   Komodo komutlarını ./ ile başlatmak zorunda değilsiniz, komodod ve komodo-cli komutlarını direkt çalıştırabilirsiniz. Örnek: `komodod`
*   Wallet dosyasını import etmek veya oluşturmak için, sonra da mining veya staking'e başlamak için https://github.com/marmarachain/Marmara-v.1.0 adresinden devam ediniz. (Marmara kurulumunu atylayınız)
