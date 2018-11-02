preCICE Webpage https://www.precice.org/

## Local development 
The website is using [Jekyll](https://jekyllrb.com/) static website generator and [Github pages](https://pages.github.com/). 
To run and develop it locally you would need [Ruby](https://www.ruby-lang.org/en/) and [Bundler](https://bundler.io/). 
With Ruby, you can install bundler using `gem install bundler`. 

After that all you need is: 

```
git clone https://github.com/precice/precice.github.io && cd precice.github.io
printf "source 'https://rubygems.org'\ngem 'github-pages', group: :jekyll_plugins " > Gemfile
bundle install
bundle exec jekyll serve
```
You can now view website locally in your browser at http://localhost:4000 

## SASS

We use the front-end framework foundation 6.4.5.
The sass files are located  in `_sass`, the main settings file is `_settings.scss`.
Due to the restrictions of jekyll's strict mode we are not allowed to specify multiple search paths.
Thus, the sass-roots of foundation and its dependecies `stylesheets` and `normalize` are merged in the folder.

The folder `precice` contains further project specific files, these are all imported by `_precice.scss` at the root.

`css/main.scss` is the main file that will be compiled into the provided css file.
