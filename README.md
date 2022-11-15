# XeroLinux "G" ISO Repo

Repo for **XeroLinux-G** ISO. Feel free to go through files and learn how it's all done. To build ISO need to use **ABS** Script via guide below, and **DO NOT** install in a VM yet there's currently an issue with *Mutter* & latest *mesa* drivers, waiting for a fix upstream. ;)

### Note
> This here, is a side project, as a result, it will only be updated every Major release of GNOME. 
> This uses R43.1 so next release will be once R44.1 lands sometime in March 2023...
-----------------------------------------------------------------

![XeroLinux-Calamares](https://i.imgur.com/LhoMdrI.png)

### Step 1 - Get Repo in to build :

Before we get started we will need to get the **ABS** repo in, that's where the new build tool is located. To do so need to edit the "pacman.conf" :

```
sudo nano /etc/pacman.conf
```

Now we need to add the repo at the end of the file, so add this,
```
# Valen Repository
[valen_repo]
SigLevel = Never
Server = https://keyaedisa.github.io/$repo/$arch
```
Now install the tool via,
```
sudo pacman -S abs
```
### Step 2 - Clone Build Repo :

Once you got Repos in, time to grab the build environment that you will be building from. Just note that you will need Git installed in order to do that.

**Install Git with :**
```
sudo pacman -S git
```
**Grab Build Env.**
```
cd ~ && git clone https://github.com/xerolinux/xero_g_iso.git
```

### Step 3 - Building the Xero ISO :

Now that we have build environment on our system, it's time to build it.

**Build ISO :**
```
cd ~/xero_iso/ && abs XeroG
```

I hope this helps.. In case of other issues kindly find me on [**Discord**](https://discord.gg/Xg6T78ahtK)

Happy building
