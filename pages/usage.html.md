**Massimo** sites are built using the command line. Run `massimo help` or `massimo help [command]` for more detailed usage information. All commands can be abbreviated, for example `new` can be called with `n`, and `watch` with `w`.


New
---

The first step after installation is to generate a new project. This can be done with the `new` command:

    massimo new my-site-name
    
This will create a folder with the basic structure of a massimo project.
    
    
Build
-----
    
After you've generated a **massimo** project and created some pages, you can build your site by runninging the `build` command. This will build the site into the public directory by default.

    cd my-site-name
    massimo build
    
    
Watch
-----

Running that command over and over again would been a pain the arse, so **massimo** can just watch for changes automatically build your site when needed:

    massimo watch
    

Server
------

Like the other static website generators, **massimo** comes with a server. Unlike the others, it's a [Rack](http://rack.rubyforge.org/) application. When a request is made, the server will check for file changes and rebuild the site if necessary. To launch the server from the command line, use the `server` command:

    massimo server
    # defaults to port 3000
    massimo server 5000
    # uses port 5000
    