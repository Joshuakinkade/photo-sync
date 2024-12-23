# Photo Sync

A simple service for syncing photos from a directory on my computer to an s3 (or compatible service) bucket.

## Usage

Normally, it'll just run as a systemd service, but I want to be able to run it from the command line for the first sync.



## Things to Consider

- It'll need to know what directory to use for syncing. What's the best way to store this? This should be per user.
- Need a list of image formats, although for my purpose .nef and .jpeg/.jpg would be sufficient
- How much cpu will this use when idle?
- How much ram will this use? Could the intial sync use too much?
- Do I want to detect changes on S3 and pull the files down? I would probably need to reconcile conflicts in that case.
