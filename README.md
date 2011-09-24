# get started

To get the list of available actions just call **diana** without parameters.

The daemon script is called **dad**.

**diana** is written in Python and uses the JSON RPC interface to communicate to the **aria2** daemon.

# tricks

If you want to download only certain files inside a torrent :

- Get the index of the relevant files with **tl**:

    tl () {
            aria2c -S "$@" | grep '\./'
    }

- Call **diana** with the appropriate option (see the manual for **aria2c** and search for **--select-file**):

    diana --select-file=foo add bar.torrent
