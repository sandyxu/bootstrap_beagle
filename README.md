# BootstrapBeagle

Welcome to your new gem! In this directory, you'll find the files you need to be able to package up your Ruby library into a gem. Put your Ruby code in the file `lib/bootstrap_beagle`. To experiment with that code, run `bin/console` for an interactive prompt.

TODO: Delete this and the text above, and describe your gem

## Installation

Add this line to your application's Gemfile:

```ruby
gem "bootstrap_beagle", git: "http://gitlab.ikcrm.com/gems/bootstrap_beagle.git"
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install bootstrap_beagle

## Usage

从模板资源文件转换成 ruby gem 的过程如下：

1. 图片资源文件从 beagle-v1.7.0/src/assets/img 放到 app/assets/images/img
2. demo页面有关的js文件从 beagle-v1.7.0/src/js/*.js 放到 app/assets/javascripts/
3. demo页面有关的css文件从 beagle-v1.7.0/src/sass/*.scss 放到 app/assets/stylesheets/
4. demo页面的外部引文文件都集中在 beagle-v1.7.0/dist/html/assets/lib/ 每个插件包是按照 html 页面访问的路径放置到了js和 css同一层级文件夹中，但是转换成 ruby gem时按照rails的规范 js 和 css要拆分到 vendor/assets/javascriptions/ 和 vendor/assets/stylesheets/ 2个不同的文件夹中存放。
5. 修改css中字体font引用路径替换成 asset_path('material-design-icons/fonts/xx') asset_path('summernote/fonts/xx')
6. 修改 config/beagle-variables.scss 文件中的$img-path，$fonts-path，$lib-path，$bootstrap-path

## Development

After checking out the repo, run `bin/setup` to install dependencies. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/[USERNAME]/bootstrap_beagle. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.

## Code of Conduct

Everyone interacting in the BootstrapBeagle project’s codebases, issue trackers, chat rooms and mailing lists is expected to follow the [code of conduct](https://github.com/[USERNAME]/bootstrap_beagle/blob/master/CODE_OF_CONDUCT.md).
