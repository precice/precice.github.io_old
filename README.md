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
