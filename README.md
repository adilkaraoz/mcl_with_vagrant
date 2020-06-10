# English
This repository run the vagrant image (Ubuntu 20.04) which contains requirements for running MCL mining or staking. You can look at http://marmara.io for information.
Komodo updated to hard forked version at 10.06.2020.

## Requirements
*   install virtual box from https://www.virtualbox.org/wiki/Downloads
*   install vagrant from https://www.vagrantup.com/downloads
*   clone this repository with `git clone https://github.com/adilkaraoz/mcl_with_vagrant.git` or download as zip and open somewhere.

## Steps to start
*   Enter the repository folder you cloned or extracted.
*   Change WORKER_COUNT at Vagrantfile or leave as is (according to machine count you want to run)
*   Run `vagrant up` wait for downloading box and running virtual machine
*   You can connect to virtual machine with `vagrant ssh worker01`command. Change 01 as 02, 03 etc. which virtual machine you want to connect
*   Follow the step at https://github.com/marmarachain/Marmara-v.1.0 to create or import your wallet then start mining or staking. (Skip Marmara Setup)

## Notes
*   At the first run, it takes some time to download image and bootstap file. (downloading blocks)
*   You don't have to use the komodo commands with ./, komodod and komodo-cli already added to your path. So, you can run with `komodod` directly
*   If you want to run Ubuntu 18.04 download https://github.com/adilkaraoz/mcl_with_vagrant/archive/0.0.2.zip and extract. Follow same steps above.
*   If you want to run Ubuntu 16.04 download https://github.com/adilkaraoz/mcl_with_vagrant/archive/v0.0.1.zip and extract. Follow same steps above.

## Donate
if you like this configuration you can take me a coffee.

### MCL wallet address
RTR3gNmYdTKY9RmM9CJzbp1KJ5MU4z6UGr
### KMD wallet address
RVj4VBWcrWyAPFqiZiGt17QrXxpFNeZKSn

# Türkçe
Bu repo tüm MCL mining veya staking yapmak için gereksinimleri içeren Ubuntu 20.04 vagrant imajını içerir. Detaylı bilgiyi http://marmara.io adresinde bulabilirsiniz.
Komodo Hard Fork sürümü 10.06.2020 ile güncellenmiştir.

## Gereklilikler
*   https://www.virtualbox.org/wiki/Downloads adresinden Virtual Box'ı indirin ve yükleyin.
*   https://www.vagrantup.com/downloads adresinden Vagrant'ı indirin ve yükleyin.
*   Bu repo'yu `git clone https://github.com/adilkaraoz/mcl_with_vagrant.git` komutu ile klonlayın veya zip olarak indirip bir yere ayıklayın.

## Başlamak için adımlar
*   Repo'yu indirdiğiniz veya klonladığınız yere gidip klasör içerisine girin.
*   Vagrantfile dosyasındaki WORKER_COUNT değerini ne kadar makine çalıştıracaksanız o şekilde değiştirin veya olduğu gibi bırakın.
*   `vagrant up` komutunu çalıştırın ve imajın indirilmesi ve çalıştırılmasına kadar bekleyin.
*   Sanal makineye `vagrant ssh worker01` komutu ile bağlanabilirsiniz. 01 değerini, hangi makineye bağlanacaksanız o şekilde değiştirin.
*   Wallet dosyasını import etmek veya oluşturmak için, sonra da mining veya staking'e başlamak için https://github.com/marmarachain/Marmara-v.1.0 adresinden devam ediniz. (Marmara kurulumunu atylayınız)

## Notlar
*   ilk çalıştırma imajı ve blokları indirmek için biraz zaman alabilir.
*   Komodo komutlarını ./ ile başlatmak zorunda değilsiniz, komodod ve komodo-cli komutlarını direkt çalıştırabilirsiniz. Örnek: `komodod`
*   Eğer Ubuntu 18.04 çalıştırmak istiyorsanız, https://github.com/adilkaraoz/mcl_with_vagrant/archive/0.0.2.zip indirin ve ayıklayın. Yukarıki aynı adımları takip edin.
*   Eğer Ubuntu 16.04 çalıştırmak istiyorsanız, https://github.com/adilkaraoz/mcl_with_vagrant/archive/v0.0.1.zip indirin ve ayıklayın. Yukarıki aynı adımları takip edin.

## Bağış
Eğer bu konfigrasyonu sevmişseniz, bana bir kahve ısmarlayabilirsiniz.

### MCL adresim
RTR3gNmYdTKY9RmM9CJzbp1KJ5MU4z6UGr
### KMD adresim
RVj4VBWcrWyAPFqiZiGt17QrXxpFNeZKSn
