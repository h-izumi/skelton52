# skelton52

My Ruby on Rails 5.2 boilerplate.

* Ruby 2.6.0
* Ruby on Rails 5.2
  * `rails new . -d mysql --webpack=react --skip-coffee --skip-turbolinks -T`
* Sprockets 4
  * with [Ruby Babel Transpiler](https://github.com/babel/ruby-babel-transpiler)
* Webpacker
  * with React
* Haml
  * with [Hamlit](https://github.com/k0kubun/hamlit)
* dotenv
* Bootstrap 4 with **no jQuery**
  * with [bootstrap.native](https://thednp.github.io/bootstrap.native/)
* Font-Awesome
* RSpec
* etc...

## How to use

Use [setup.rb](https://raw.githubusercontent.com/h-izumi/skelton52/master/setup.rb):

```shell
cd /path/to/app-parent
curl -L https://raw.githubusercontent.com/h-izumi/skelton52/master/setup.rb | APP_NAME="app-name" ruby
```

* Set `NO_COMMIT=true` to skip `git commit`.

```shell
curl -L https://raw.githubusercontent.com/h-izumi/skelton52/master/setup.rb | APP_NAME="app-name" NO_COMMIT=true ruby
```

or Manually:

```shell
cd /path/to/app-parent
curl -L -o skelton52.zip https://github.com/h-izumi/skelton52/archive/master.zip
unzip skelton52.zip
mv skelton52-master app-name
rm skelton52.zip
cd app-name
find . -type f -print0 | xargs -0 sed -i -e 's/SKELTON52/APP_NAME/g'
find . -type f -print0 | xargs -0 sed -i -e 's/skelton52/app_name/g'
find . -type f -print0 | xargs -0 sed -i -e 's/Skelton52/AppName/g'
rm README.md
rm LICENSE.txt
rm setup.rb
git init
git add .
git commit -m "initial."
```

If use on macOS, you should set argument ` ''` after `sed -i`, like `sed -i '' -e`.

## License

[CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/deed).

You probably should remove `LICENSE.txt` file when use this repo on your work.
