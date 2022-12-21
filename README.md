# XeroLinux "G" ISO Repo

Repo for the **Xero-G** Project. Feel free to go through files and learn how it's all done. To build ISO need to use **ABS** Script via guide below. [Click Here](https://forum.xerolinux.xyz/thread-201.html) for full release info ;)

<p align="center">
    <img width="300" src="https://i.imgur.com/QWqMIsr.png" alt="logo">
</p>

<h1 align="center">You must be on an *Arch* based Distro to build ISO.</h1>

> The following are not supported Distros to build on since they
> don't use Arch repos which will result in errors building the ISO.
> - Manjaro (Own Repos)
> - CachyOS (Arch v3)
> - KaOS (Limited Repos)
> - Artix (No Systemd)
-----------------------------------------------------------------
### Note
> As it stands, there will be no public ISO of this project. Building it yourselves, is currently the *only* way to get it for *Free*. Or wait until I have raised enough to make it join the family. However, an ISO will be made available, as well as many other bonuses,
> on **Patreon**, via our [**Platinum Tier**](https://www.patreon.com/XeroLinux/membership) (monthly). Or if you find that amount to be too much or don't want to support the project on a monthly basis, you can donate any amount to my [**FundRaizr**](https://fnd.us/523mC5) (Once) without any bonuses, just ISO. <sup>[**`Why Paid ?`**](https://github.com/xerolinux/xero_g_iso/blob/main/support.md)</sup>
-----------------------------------------------------------------

<h1 align="center">.:: Video Guide ::.</h1>

<p align="center">

   <a href="https://youtu.be/DBU3pmeF9p8" target="_blank" title="Video Guide"><img src="https://i.imgur.com/GXx8Oq2.png" alt="Watch Video Guide" /></a>

</p>

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
cd ~/xero_g_iso/ && abs XeroG
or
cd ~/xero_g_iso/ && abs -xg
```

Follow the prompts and you good to go...

I hope this helps.. In case of other issues kindly find me on [**Discord**](https://discord.gg/Xg6T78ahtK)

Happy building
