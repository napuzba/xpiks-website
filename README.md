#xpiks


## Usage Locally**

Run local server by invoking:

    $ hugo server
    port 1313 already in use, attempting to use an available port
    Building sites …
    ...
    Web Server is available at http://localhost:49818/ (bind address 127.0.0.1)

The site will be available at http://localhost:1313


## Generate static site

Generate local site by invoking:

    $ rm -r public
    $ hugo

    Building sites …
                     | EN
    +------------------+-----+
    Pages            |  96
    Paginator pages  |   7
    Non-page files   |   0
    Static files     | 212
    Processed images |   0
    Aliases          |   1
    Sitemaps         |   1
    Cleaned          |   0

    Total in 1310 ms

The public folder contains the static site.