# Ruby style guide

The [rubocop configuration](https://github.com/livestax/liveshack/blob/master/.rubocop.yml)
in the Liveshack repo serves as our styleguide.

Rubocop is run as part of the default rake task and on CircleCi. You can also run the Rubocop task on its own:

`bundle exec rake rubocop:run`

In addition to the cop rules in `.rubocop.yml`, there are some files which have their own exceptions. These can be found by searching for `rubocop:disable` in the Liveshack repo. 

For example, in [debug_steps.rb](https://github.com/livestax/liveshack/blob/master/features/step_definitions/debug_steps.rb) the `Lint/Debugger` cop is disabled, as the presence of calls to the debugger in this file is not an error.

```
# rubocop:disable Lint/Debugger
Then(/^take a screenshot$/) do
  sleep 1
  save_and_open_screenshot
end

Then(/^open the page$/) do
  save_and_open_page
end
# rubocop:enable Lint/Debugger
```
More information about Rubocop can be found in the [Rubocop documentation](http://www.rubydoc.info/github/bbatsov/rubocop/).
