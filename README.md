
Scripts to build and operate a Hackage2 server.

### Synopsis

    # download and build hackage-server
    $ ./build-sandbox

    $ mkdir server-1
    (...edit ./server ...)

    $ ./server check-config
    $ ./server init
    $ ./server start
    $ ./server pid

    # Make 'admin' an uploader
    $ ./server add-uploader admin

    # Add a new user
    $ ./server add-user "Real Name" "username" "email@address.com"

If sendmail is not configured, check the sendmail queue for the
confirmation email.

### ./server

The script `./server` is a convenience script to operate an instance
of a Hackage server.

To configure, open it in an editor and set the following shell variables:

    HACKAGE_SOURCE=...  -- path to the hackage-server source tree
    HACKAGE_SERVER=...  -- path to the hackage-server binary
    HACKAGE_MIRROR=...  -- path to the hackage-mirror binary
    SERVER_DIR=...      -- root directory of the server instance
    SERVER_PORT=...     -- server port

Use `./server help` for a list of supported command. See the SYMOPSIS section
for examples of usage.

### Tidbits

Places to look for the sendmail queue directory:

- (OS X) /var/spool/postfix/active
- (Linux) /var/spool/mqueue

