# django-sass-processor
* Annoyed having to run a Compass, Grunt or Gulp daemon while developing Django projects?
Well, then this app is for you! Compile SASS/SCSS files on the fly without having to manage third party services nor special IDE plugins.
# Other good reasons for using this library
* Refer SASS/SCSS files directly from your sources, instead of referring a compiled CSS file, having to rely on another utility which creates them from SASS/SCSS files, hidden in your source tree.
* Use Django's settings.py for the configuration of paths, box sizes etc., instead of having another SCSS specific file (typically _variables.scss), to hold these.
* Extend your SASS functions by calling Python functions directly out of your Django project.
* View SCSS errors directly in the debug console of your Django's development server.
