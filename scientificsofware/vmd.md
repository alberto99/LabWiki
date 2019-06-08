<!-- TITLE: Vmd -->
<!-- SUBTITLE: A quick summary of Vmd -->

# Running vmd locally accessing remote files
Finally figured out how to run vmd from linux -- Thanks to Vini from the Roitberg group for his help

Basically you mount a filesystem into your local linux (ubuntu) machine:

```
mkdir Hypergator
sshfs UF:/ufrc/alberto.perezant/your_user_name  Hypergator
```
Now you can access anything that is in Hypergator as if it were local. So you can run vmd locally to open the files (you will have to download and install vmd If you have not).

When you are done and you want to unmount hypergator from your computer:
```
fusermount -u Hypergator
```
(For this to work you have to make sure you are no longer in the Hypergator directory or using it in any way).

You might not have sshfs installed, to get it run:
```
sudo apt-get install sshfs
```