[![Stories in Ready](https://badge.waffle.io/fcvarela/pyremotezip.png?label=ready&title=Ready)](https://waffle.io/fcvarela/pyremotezip)
# PyRemoteZip

PyRemoteZip is a pure python module to extract files from remote zip archives without downloading the whole zip archive.

### Usage

        from pyremotezip import RemoteZip
        rz = RemoteZip(<some_url_here>)
        toc = rz.getTableOfContents()
        
        # want file at pos 2
        output = rz.extractFile(toc[2]['filename'])

### Contributing

Have you forked and improved this? Please submit your pull requests and raise issues here!

### Warning

* remotezip need http's Content-Range feature.[Content-Range](http://www.w3.org/Protocols/rfc2616/rfc2616-sec14.html#sec14.16)
* Can't support zip file > 4G, or compressed file >4G, temporarily. Next plan is adding zlib64 supporting.
