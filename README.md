***Initial  Setup***
1. Yeoman    http://yeoman.io/
npm install -g yo
  1.1. Install.    yeoman/generator-webapp
    https://github.com/yeoman/generator-webapp

            Install: npm install --global yo gulp-cli bower generator-webapp
            Run yo webapp to scaffold your webapp
            Run gulp serve to preview and watch for changes
            Run bower install --save <package> to install frontend dependencies
            Run gulp serve:test to run the tests in the browser
            Run gulp to build your webapp for production
            Run gulp serve:dist to preview the production build

2.  Installation of  HEXO git  Blog generator :  https://hexo.io/

            npm install hexo-cli -g
            hexo init blog
            cd blog
            npm install
            hexo server




  **Development of the Frontend**

  1. Downloaded free BootStrap Theme to kick-start development.
        https://startbootstrap.com/template-overviews/stylish-portfolio/

       see new sub- directory:  Themes/stylish-portfolio......



*** OPTIONAL  Ruby on Rails ****

     Install Ruby  & gem & Ruby DevKit
            Try to use Chocolatey    ( The sane way to manage software on Windows ):       https://chocolatey.org/

    Win7 "chocolatery"  installation:   
  1. cmd.exe  
  2. <ctrl><shift><enter>    Switch cmd.exe into the Administrator mode.
  3. @powershell -NoProfile -ExecutionPolicy Bypass -Command "iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"
          ( https://chocolatey.org/install
          https://www.howtogeek.com/howto/windows-vista/run-a-command-as-administrator-from-the-windows-vista-run-box/)
     C:\> choco upgrade chocolatey

  4.    Then install Ruby as described in   https://chocolatey.org/packages/ruby
      From admin cmd.exe:
                  1. cmd.exe  
                  2. <ctrl><shift><enter>
        C:\> choco install ruby
                ................
                Ruby is going to be installed in 'C:\tools\ruby23'
                Installing 64-bit ruby...
                ruby has been installed.
                Environment Vars (like PATH) have changed. Close/reopen your shell to
                 see the changes (or in powershell/cmd.exe just type `refreshenv`).
                 The install of ruby was successful.
                  Software installed to 'C:\tools\ruby23\'

                  Chocolatey installed 2/2 packages. 0 packages failed.
                   See the log for details (C:\ProgramData\chocolatey\logs\chocolatey.log).

          C:\>refreshenv
                    Refreshing environment variables from registry for cmd.exe. Please wait...Finished..
          C:\>choco upgrade ruby
                            Chocolatey v0.10.5
                            Upgrading the following packages:
                            ruby
                            By upgrading you accept licenses for the packages.
                            ruby v2.3.3 is the latest version available based on your source(s).

                            Chocolatey upgraded 0/1 packages. 0 packages failed.
                             See the log for details (C:\ProgramData\chocolatey\logs\chocolatey.log).

                            C:\>
          Run ruby, gem versions check:
                            C:\Users\Vlad\Documents\PROG\HTML5\NK (initYoman)
                            λ ruby -v
                            ruby 2.3.3p222 (2016-11-21 revision 56859) [x64-mingw32]

                            C:\Users\Vlad\Documents\PROG\HTML5\NK (initYoman)
                            λ gem -v
                            2.5.2
        Ruby DevKit install:
                         https://chocolatey.org/packages/ruby2.devkit

                        Run from Powershell as administrator:
                      PS C:\> choco install ruby2.devkit
                              Chocolatey v0.10.5
                              Installing the following packages:
                              ruby2.devkit
                              By installing you accept licenses for the packages.
                              Progress: Downloading 7zip.commandline 16.02.0.20170209... 100%
                              Progress: Downloading 7zip.portable 16.04... 100%
                              Progress: Downloading ruby2.devkit 4.7.2.2013022402... 100%

                              7zip.portable v16.04 [Approved]
                              7zip.portable package files install completed. Performing other installation steps.
                              The package 7zip.portable wants to run 'chocolateyInstall.ps1'.
                              Note: If you don't run this script, the installation will fail.
                              Note: To confirm automatically next time, use '-y' or consider:
                              choco feature enable -n allowGlobalConfirmation
                              Do you want to run the script?([Y]es/[N]o/[P]rint): y

                              Installing 64 bit version
                              Extracting C:\ProgramData\chocolatey\lib\7zip.portable\tools\7zip_x64.exe to C:\ProgramData\chocolatey\lib\7zip.portable
                              \tools...
                              C:\ProgramData\chocolatey\lib\7zip.portable\tools
                              Extracting C:\ProgramData\chocolatey\lib\7zip.portable\tools\7zip_extra.7z to C:\ProgramData\chocolatey\lib\7zip.portabl
                              e\tools\7z-extra...
                              C:\ProgramData\chocolatey\lib\7zip.portable\tools\7z-extra
                              ShimGen has successfully created a shim for 7z.exe
                              ShimGen has successfully created a shim for 7zFM.exe
                              ShimGen has successfully created a shim for 7zG.exe
                              ShimGen has successfully created a shim for 7za.exe
                              The install of 7zip.portable was successful.
                              Software installed to 'C:\ProgramData\chocolatey\lib\7zip.portable\tools\7z-extra'

                              7zip.commandline v16.02.0.20170209 [Approved]
                              7zip.commandline package files install completed. Performing other installation steps.
                              The install of 7zip.commandline was successful.
                              Software install location not explicitly set, could be in package or
                              default install location if installer.

                              ruby2.devkit v4.7.2.2013022402 [Approved] - Possibly broken
                              ruby2.devkit package files install completed. Performing other installation steps.
                              The package ruby2.devkit wants to run 'chocolateyInstall.ps1'.
                              Note: If you don't run this script, the installation will fail.
                              Note: To confirm automatically next time, use '-y' or consider:
                              choco feature enable -n allowGlobalConfirmation
                              Do you want to run the script?([Y]es/[N]o/[P]rint): y

                              Get-BinRoot is going to be deprecated in v1 and removed in v2. It has been replaced with Get-ToolsLocation (starting wit
                              h v0.9.10), however many packages no longer require a special separate directory since package folders no longer have ve
                              rsions on them. Some do though and should continue to use Get-ToolsLocation.
                              Chocolatey is installing DevKit to C:\tools\DevKit2
                              Please wait...
                              DevKit2
                              ruby.devkit
                              WARNING: Url has SSL/TLS available, switching to HTTPS for download
                              Downloading ruby2.devkit 64 bit
                              from 'https://cdn.rubyinstaller.org/archives/devkits/DevKit-mingw64-64-4.7.2-20130224-1432-sfx.exe'
                              Progress: 100% - Completed download of C:\Users\Vlad\AppData\Local\Temp\chocolatey\chocolatey\ruby.devkit\ruby.devkitIns
                              tall.exe (42.22 MB).
                              Download of ruby.devkitInstall.exe (42.22 MB) completed.
                              Hashes match.
                              C:\Users\Vlad\AppData\Local\Temp\chocolatey\chocolatey\ruby.devkit\ruby.devkitInstall.exe
                              Removing legacy install devkit items from C:\tools\ruby23\bin if they exist
                              Cleaning out the contents of C:\tools\DevKit2
                              Extracting the contents of C:\Users\Vlad\AppData\Local\Temp\chocolatey\chocolatey\ruby.devkit\ruby.devkitInstall.exe to
                              C:\tools\DevKit2
                              You may want to configure your config.yml after this installation and rerun 'cinst ruby.devkit' if the defaults do not m
                              eet your needs
                              Initializing and installing DevKit into Ruby.

                              Initialization complete! Please review and modify the auto-generated
                              'config.yml' file to ensure it contains the root directories to all
                              of the installed Rubies you want enhanced by the DevKit.
                              Invalid configuration or no Rubies listed. Please fix 'config.yml'
                              and rerun 'ruby dk.rb install'
                              WARNING: Write-ChocolateySuccess is deprecated and will be removed in v2. If you are the maintainer, please remove it fr
                              om your package file.
                              The install of ruby2.devkit was successful.
                              Software install location not explicitly set, could be in package or
                              default install location if installer.

                              Chocolatey installed 3/3 packages. 0 packages failed.
                              See the log for details (C:\ProgramData\chocolatey\logs\chocolatey.log).
                              PS C:\>

                              From Admin cmd.exe check installation:
                              C:\>choco list -l ruby
                              Chocolatey v0.10.5
                              chocolatey 0.10.5
                              ruby 2.3.3
                              ruby2.devkit 4.7.2.2013022402
                              3 packages installed.

                              C:\>


        Install Rails AFTER Ruby DevKit installation.:
                  https://www.tutorialspoint.com/ruby-on-rails/rails-installation.htm

        From cmder console ( cmd.exe NOT  administrator privilege )
        1. Add  Ruby DevKit2 to the PATH
            C:\Users\Vlad\Documents\PROG\HTML5\rubyrails
                  λ  c:\tools\DevKit2\devkitvars.bat
                        Adding the DevKit to PATH...

        2. Install  Rails
            C:\Users\Vlad\Documents\PROG\HTML5\rubyrails
                λ gem install rails
                ...
                Done installing documentation for nio4r, websocket-extensions, websocket-driver, actioncable, thor, method_source, railties, bundler, sprockets, sprockets-rails, rails after 44 seconds
                11 gems installed
        3.    Check Rails version:
        C:\Users\Vlad\Documents\PROG\HTML5\rubyrails
              λ rails -v
              Rails 5.1.1

        4.   Update Rails
        C:\Users\Vlad\Documents\PROG\HTML5\rubyrails
              λ gem update rails
              Updating installed gems
              Nothing to update

        5.  Run demo project

                      C:\Users\Vlad\Documents\PROG\HTML5\rubyrails
                      λ rails new demo
                            create
                            create  README.md
                            create  Rakefile
                            create  config.ru
                            create  .gitignore
                            create  Gemfile
                               run  git init from "."
                      Initialized empty Git repository in C:/Users/Vlad/Documents/PROG/HTML5/rubyrails/demo/.git/
                            create  app
                            create  app/assets/config/manifest.js
                            create  app/assets/javascripts/application.js
                            create  app/assets/javascripts/cable.js
                            create  app/assets/stylesheets/application.css
                            create  app/channels/application_cable/channel.rb
                            create  app/channels/application_cable/connection.rb
                            create  app/controllers/application_controller.rb
                            create  app/helpers/application_helper.rb
                            create  app/jobs/application_job.rb
                            create  app/mailers/application_mailer.rb
                            create  app/models/application_record.rb
                            create  app/views/layouts/application.html.erb
                            create  app/views/layouts/mailer.html.erb
                            create  app/views/layouts/mailer.text.erb
                            create  app/assets/images/.keep
                            create  app/assets/javascripts/channels
                            create  app/assets/javascripts/channels/.keep
                            create  app/controllers/concerns/.keep
                            create  app/models/concerns/.keep
                            create  bin
                            create  bin/bundle
                            create  bin/rails
                            create  bin/rake
                            create  bin/setup
                            create  bin/update
                            create  bin/yarn
                            create  config
                            create  config/routes.rb
                            create  config/application.rb
                            create  config/environment.rb
                            create  config/secrets.yml
                            create  config/cable.yml
                            create  config/puma.rb
                            create  config/environments
                            create  config/environments/development.rb
                            create  config/environments/production.rb
                            create  config/environments/test.rb
                            create  config/initializers
                            create  config/initializers/application_controller_renderer.rb
                            create  config/initializers/assets.rb
                            create  config/initializers/backtrace_silencers.rb
                            create  config/initializers/cookies_serializer.rb
                            create  config/initializers/cors.rb
                            create  config/initializers/filter_parameter_logging.rb
                            create  config/initializers/inflections.rb
                            create  config/initializers/mime_types.rb
                            create  config/initializers/new_framework_defaults_5_1.rb
                            create  config/initializers/wrap_parameters.rb
                            create  config/locales
                            create  config/locales/en.yml
                            create  config/boot.rb
                            create  config/database.yml
                            create  db
                            create  db/seeds.rb
                            create  lib
                            create  lib/tasks
                            create  lib/tasks/.keep
                            create  lib/assets
                            create  lib/assets/.keep
                            create  log
                            create  log/.keep
                            create  public
                            create  public/404.html
                            create  public/422.html
                            create  public/500.html
                            create  public/apple-touch-icon-precomposed.png
                            create  public/apple-touch-icon.png
                            create  public/favicon.ico
                            create  public/robots.txt
                            create  test/fixtures
                            create  test/fixtures/.keep
                            create  test/fixtures/files
                            create  test/fixtures/files/.keep
                            create  test/controllers
                            create  test/controllers/.keep
                            create  test/mailers
                            create  test/mailers/.keep
                            create  test/models
                            create  test/models/.keep
                            create  test/helpers
                            create  test/helpers/.keep
                            create  test/integration
                            create  test/integration/.keep
                            create  test/test_helper.rb
                            create  test/system
                            create  test/system/.keep
                            create  test/application_system_test_case.rb
                            create  tmp
                            create  tmp/.keep
                            create  tmp/cache
                            create  tmp/cache/assets
                            create  vendor
                            create  vendor/.keep
                            create  package.json
                            remove  config/initializers/cors.rb
                            remove  config/initializers/new_framework_defaults_5_1.rb
                               run  bundle install
                      Fetching gem metadata from https://rubygems.org/..........
                      Fetching version metadata from https://rubygems.org/..
                      Fetching dependency metadata from https://rubygems.org/.
                      Resolving dependencies....
                      Installing rake 12.0.0
                      Using concurrent-ruby 1.0.5
                      Using i18n 0.8.1
                      Installing minitest 5.10.2
                      Using thread_safe 0.3.6
                      Using builder 3.2.3
                      Using erubi 1.6.0
                      Using mini_portile2 2.1.0
                      Using rack 2.0.2
                      Using nio4r 2.0.0
                      Using websocket-extensions 0.1.2
                      Using mime-types-data 3.2016.0521
                      Using arel 8.0.0
                      Installing public_suffix 2.0.5
                      Installing bindex 0.5.0 with native extensions
                      Using bundler 1.14.6
                      Installing byebug 9.0.6 with native extensions
                      Installing ffi 1.9.18 (x64-mingw32)
                      Installing coffee-script-source 1.12.2
                      Installing execjs 2.7.0
                      Using method_source 0.8.2
                      Using thor 0.19.4
                      Installing multi_json 1.12.1
                      Installing puma 3.8.2 with native extensions
                      Installing rubyzip 1.2.1
                      Installing sass 3.4.23
                      Installing tilt 2.0.7
                      Installing websocket 1.2.4
                      Installing sqlite3 1.3.13 (x64-mingw32)
                      Installing turbolinks-source 5.0.3
                      Using tzinfo 1.2.3
                      Using nokogiri 1.7.2 (x64-mingw32)
                      Using rack-test 0.6.3
                      Using sprockets 3.7.1
                      Using websocket-driver 0.6.5
                      Using mime-types 3.1
                      Installing addressable 2.5.1
                      Installing childprocess 0.7.0
                      Installing coffee-script 2.4.1
                      Installing uglifier 3.2.0
                      Installing turbolinks 5.0.1
                      Using activesupport 5.1.1
                      Installing tzinfo-data 1.2017.2
                      Using loofah 2.0.3
                      Installing xpath 2.0.0
                      Using mail 2.6.5
                      Installing selenium-webdriver 3.4.0
                      Using rails-dom-testing 2.0.3
                      Using globalid 0.4.0
                      Using activemodel 5.1.1
                      Installing jbuilder 2.6.4
                      Using rails-html-sanitizer 1.0.3
                      Installing capybara 2.14.0
                      Using activejob 5.1.1
                      Using activerecord 5.1.1
                      Using actionview 5.1.1
                      Using actionpack 5.1.1
                      Using actioncable 5.1.1
                      Using actionmailer 5.1.1
                      Using railties 5.1.1
                      Using sprockets-rails 3.2.0
                      Installing coffee-rails 4.2.1
                      Installing web-console 3.5.1
                      Using rails 5.1.1
                      Installing sass-rails 5.0.6
                      Bundle complete! 13 Gemfile dependencies, 65 gems now installed.
                      Use `bundle show [gemname]` to see where a bundled gem is installed.

                      C:\Users\Vlad\Documents\PROG\HTML5\rubyrails
                      λ

    6. Start  DEMO server
                    C:\Users\Vlad\Documents\PROG\HTML5\rubyrails
                    λ cd demo

                    C:\Users\Vlad\Documents\PROG\HTML5\rubyrails\demo (master)
                    λ rails server
                    => Booting Puma
                    => Rails 5.1.1 application starting in development on http://localhost:3000
                    => Run `rails server -h` for more startup options
                    *** SIGUSR2 not implemented, signal based restart unavailable!
                    *** SIGUSR1 not implemented, signal based restart unavailable!
                    *** SIGHUP not implemented, signal based logs reopening unavailable!
                    Puma starting in single mode...
                    * Version 3.8.2 (ruby 2.3.3-p222), codename: Sassy Salamander
                    * Min threads: 5, max threads: 5
                    * Environment: development
                    * Listening on tcp://0.0.0.0:3000
                    Use Ctrl-C to stop

      7. Success:               
                    Started GET "/" for 127.0.0.1 at 2017-05-15 09:54:56 -0400
                    Processing by Rails::WelcomeController#index as HTML
                      Rendering C:/tools/ruby23/lib/ruby/gems/2.3.0/gems/railties-5.1.1/lib/rails/templates/rails/welcome/index.html.erb
                      Rendered C:/tools/ruby23/lib/ruby/gems/2.3.0/gems/railties-5.1.1/lib/rails/templates/rails/welcome/index.html.erb (10.0ms)
                    Completed 200 OK in 1031ms (Views: 57.7ms)

   8. Now read the tutorial.      https://www.tutorialspoint.com/ruby-on-rails/rails-directory-structure.htm

   Good Luck!!!!!
