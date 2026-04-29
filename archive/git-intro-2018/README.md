# Lets Talk About Version Control

- Paper:[Excuse me, do you have a moment to talk about version control?](https://peerj.com/preprints/3159/): **[pdf](https://github.kcl.ac.uk/k0959646/version-control/raw/master/lets-talk-about-version-control-peerj-preprints-3159.pdf)**  
- Slides(Rmd format): [slides](https://github.kcl.ac.uk/k0959646/version-control/blob/master/2018-04-10-dept-talk.Rmd)  
- If you want the "fancy" html, then download or better yet clone the repo:- 

```bash
git clone https://github.kcl.ac.uk/k0959646/version-control.git
```

*****

# Something extra...Apart from using version control...

Basic set up and advice for keep your data backed up. This is a very quick rough guide...

## What you need

- external hard drive
- Google Drive
- Dropbox
- Optionally: AWS, GCE, Azure
- Git 
- GitHub Account
- University Storage and Back up
- Personal Computer

## Data Back up!

- **3-2-1 Rule** 
- A 3-2-1 strategy means having at least 3 total copies of your data, 2 of which are local but on different mediums (read: devices), and at least 1 copy offsite. ... The online backup continuously scans your computer and uploads your data offsite to a datacenter.

  
![321Backup](https://github.kcl.ac.uk/k0959646/version-control/blob/master/321-Backup.png)
  

## External HDD
- Get one for yourself and the Lab!!!  
- min 2-4TB for personal use  
  - or as much storage as you can afford
- RAID 1: min 2 disks, mirrored (see: [https://en.wikipedia.org/wiki/RAID](https://en.wikipedia.org/wiki/RAID))
- See up Automatic backup hourly/daily

**What you can get from Amazon.co.uk** (or from whomever does the ordering)
- NAS: [The 10 best NAS devices](https://www.techradar.com/news/the-10-best-nas-devices-reviewed)
- Timemachine MacOSx
- WD Mybook Duo

## Cloud Storage

- Dropbox
- Google Drive
- ASW s3 or glacier 
- Azure
- GCE
- OneDrive
- ...others?

## Institute Storage and Backup

- University Provided
- Dong trust it - make sure you use other backup solutions (i.e have more than one copy/backup of your data)

## What to do as soon as you get your raw data

- create 3 copies
- make them read only
- archive one copy - where you put it is your choice
  - inculde metadata/README: what is the data, timestamp, who, where, why,what,when,format
- store one copy on your local machine + External HDD
  - your machine will be linked of Dropbox and or Googel Drive
    - inculde metadata/README: what is the data, timestamp, who, where, why,what,when,format
  - your machine will be attached to an External HDD
- store one copy on Cloud or secure private cloud
  - inculde metadata/README: what is the data, timestamp, who, where, why,what,when,format
  

