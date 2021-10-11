This "blog" is plain ol' markdown, rendered by whatever default settings are provided by Github Pages.

It lives entirely in the cloud, not even on my local ChromeOS device. Here are the barebones notes on how to set this up.

* Open a [GCP Cloud Shell](https://cloud.google.com/shell)
  * Sign up for a GCP account (credit card required) if you don't already have one
  * Cloud Shell is part of the [Free Tier](https://cloud.google.com/free/docs/gcp-free-tier), which means your credit card won't get charged
  * You get 5GB of persistent storage
* Once you've launched a Cloud Shell, generate a new ssh key: `ssh-keygen -t ed25519 -C "your@email.address"`
* Add the public key to github: `cat .ssh/id_ed25519.pub` and [paste it into Github](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)
* Create a [Github Page](https://pages.github.com/)
* You can now clone the repo in your Cloud Shell instance: `git clone git@github.com:USERNAME/USERNAME.github.io.git`
* You can now create new files in the Cloud Shell Editor and use git in the Cloud Shell terminal to commit and push to upstream.

The VM instance goes away if it's not used in 20m, but your home directory will persist (as long as you login every 120 days). Again, this is part of the free tier, so you won't get charged.

## Yeah, but why?

After 20+ years as a professional software developer, I have a strong preference for "no compute" in my personal life. This means:

* ChromeOS devices, because I don't want to sysadmin a laptop.
* No cloud VMs, because I don't want to sysadmin, period.
* No blogging framework. Static site generators require config and work.

I guess I also don't want a hosted version of wordpress or similar, because Markdown is the least common denominator, and will hopefully be trivially portable to whatever future metaverse we get.