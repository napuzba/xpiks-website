# xpiks

## Install Tools

Install extended version of hugo for your platform. See [Install Hugo](https://gohugo.io/getting-started/installing/).

To generete optimizated static site, install Node.js for your platform. See [Install Node.js](https://nodejs.org/en/download/). Then install [hugulp](https://github.com/jbrodriguez/hugulp):

    npm install -g hugulp

## Run Local Server

In bash shell, invoke build-server

    $ ./build-server

    port 1313 already in use, attempting to use an available port
    Building sites …
    ...
    Web Server is available at http://localhost:49818/ (bind address 127.0.0.1)

The site will be available at http://localhost:1313

## Generate Static Site
 
In bash shell, invoke build
    
    $ ./build

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

## Generate Optimized Static Site

In bash shell, invoke build-dist
 
    $ ./build-dist
    
    Building sites …
                     | EN
    +------------------+-----+
    Pages            |  98
    Paginator pages  |   7
    Non-page files   |   0
    Static files     | 214
    Processed images |   0
    Aliases          |   1
    Sitemaps         |   1
    Cleaned          |   0

    Total in 1043 ms
    [00:16:05] hugulp v2.0.6
    [00:16:07] building site ... (["images","styles","scripts","fingerprint","html"])

    [00:17:48] gulp-imagemin: Minified 86 images (saved 2.34 MB - 13.8%)
    [00:17:53] html:  all files 756.22 kB