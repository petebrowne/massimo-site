**Massimo** projects can be configured through a `config.rb` file located in the root of your project or by using command line options. The config file will automatically detected when you run massimo&nbsp;[commands](/usage/).


config.rb
---------

In the `config.rb` file, you have access to all of the site's methods. For&nbsp;example:

    config.javascripts_url = '/js'
    config.stylesheets_url = '/css'
    config.output_path     = '_site'
    
    if config.environment.production?
      config.javascripts_compressor = :packr
      config.sass = { :style => :compressed }
    end
    
    resource :user do
      unprocessable
    end
    
    helpers do
      def users
        User.all
      end
    end
    
This config file does a few things:

* It changes the URLs for the javascripts and stylesheets.
* It changes the output path to `'_site'`
* Uses Packr for javascripts compression and compresses the stylesheets during production mode
* It creates a custom [resource](/resources/).
* It creates a custom helper method to access the custom resources.

*Note the `if config.environment.production?` block. This changes the configuration based on the environment setup in the command line.*
    
    
Options
-------

<table>
  <tbody>
    <tr>
      <th>source_path</th>
      <td>The path to the source files of the project. This can be changed on the command line using the <code>--source-path=PATH</code> option. Defaults to <code>'.'</code>.</td>
    </tr>
    <tr>
      <th>output_path</th>
      <td>The path to output the site to. This can be changed on the command line using the <code>--output-path=PATH</code> option. Defaults to <code>'public'</code>.</td>
    </tr>
    <tr>
      <th>environment</th>
      <td>A string representing the Site's environment. This can be changed on the command line using the <code>--environment</code> option or the <code>--production</code> flag. Defaults to <code>'development'</code>.</td>
    </tr>
    <tr>
      <th>base_url</th>
      <td>The base url of this site. You would change this if the site existed in a subdirectory. Defaults to <code>'/'</code>.</td>
    </tr>
    <tr>
      <th>[resource]_path</th>
      <td>The path to where the given resources files are located. Defaults to the name of the resource. For example, <code>pages_path</code> defaults to <code>'pages'</code>, and <code>javascripts_path</code> defaults to <code>'javascripts'</code>.</td>
    </tr>
    <tr>
      <th>[resource]_url</th>
      <td>The base url for the given resources. Defaults to <code>'/javascripts'</code> for javascripts and <code>'/stylesheets'</code> for stylesheets. Defaults to <code>'/'</code> for everything else.</td>
    </tr>
    <tr>
      <th>javascripts_compressor</th>
      <td>Which javasript compressor to use.  Available options are <code>:jsmin</code> (<a href='http://github.com/rgrove/jsmin/'>JSMin</a>), <code>:packr</code> (<a href='http://github.com/jcoglan/packr'>Packr</a>), <code>:yui</code> (<a href='http://github.com/sstephenson/ruby-yui-compressor/'>YUI::JavaScriptCompressor</a>), and <code>:closure</code> (<a href='http://github.com/documentcloud/closure-compiler/'>Closure::Compiler</a>). By default there is no compression.</td>
    </tr>
  </tbody>
</table>