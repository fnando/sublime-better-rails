# Better Rails

This is a custom Ruby package, that includes snippets, custom syntax highlighters and more!

## Installation

### Setup Package Control Repository

1. Follow the instructions from https://sublime.fnando.com.
2. Open the command pallete, run “Package Control: Install Package“, then search for “Rubocop Formatter“.
3. Install the [ApplySyntax](https://github.com/facelessuser/ApplySyntax) package and use the settings below.

By the way, there is a [Better Ruby](https://github.com/fnando/better-ruby-for-sublime-text) package as well.

### Git Clone

Clone this repository into the Sublime Text “Packages” directory, which is located where ever the “Preferences” -> “Browse Packages” option in sublime takes you.

## ApplySyntax configuration

```json
{
  "new_file_syntax": "Better Ruby/Ruby",
  "reraise_exceptions": true,

  "syntaxes": [
    {
      "syntax": "Better Ruby/Bundler",
      "rules": [
        {"file_path": ".*(\\\\|/)Gemfile$"}
      ]
    },

    {
      "syntax": "Better Ruby/Puma",
      "rules": [
        {"file_path": ".*(\\\\|/)puma\\.rb$"}
      ]
    },

    {
      "syntax": "Better Ruby/Ruby Test",
      "rules": [
        {"file_path": ".*_test\\.rb$"}
      ]
    },

    {
      "syntax": "Better Ruby/Ruby",
      "extensions": ["thor", "rake", "simplecov", "jbuilder", "rb", "podspec", "rabl"],
      "rules": [
        {"file_path": ".*(\\\\|/)Capfile$"},
        {"file_path": ".*(\\\\|/)Guardfile$"},
        {"file_path": ".*(\\\\|/)[Rr]akefile$"},
        {"file_path": ".*(\\\\|/)Berksfile$"},
        {"file_path": ".*(\\\\|/)[Cc]heffile$"},
        {"file_path": ".*(\\\\|/)Thorfile$"},
        {"file_path": ".*(\\\\|/)Podfile$"},
        {"file_path": ".*(\\\\|/)config.ru$"},
        {"file_path": ".*\\\\Vagrantfile(\\\\..*)?$"},
        {"file_path": ".*/Vagrantfile(/..*)?$"},
        {"interpreter": "ruby"}
      ]
    }
  ]
}
```
