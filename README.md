# ReadmeScore

Gives a complexity score for a README.

Example score:

| Repo                                                          | Score |
|---------------------------------------------------------------|-------|
| https://github.com/RolandasRazma/RRFPSBar                     | 16    |
| https://github.com/JRG-Developer/MediaRSSParser               | 35    |
| https://github.com/ruslanskorb/RSDayFlow                      | 35    |
| https://github.com/samnung/AFHTTPFileUpdateOperation          | 31    |
| https://github.com/schneiderandre/ASCFlatUIColor              | 65    |
| https://github.com/daltoniam/BootstrapUIKit                   | 60    |
| https://github.com/AFNetworking/AFNetworking                  | 95    |
| https://github.com/tomersh/AppleGuice                         | 85    |
| https://github.com/kevindelord/DKHelper                       | 25    |
| https://github.com/saturngod/IAPHelper                        | 75    |
| https://github.com/alskipp/ASValueTrackingSlider              | 87    |
| https://github.com/phranck/CNTreeNode                         | 25    |
| https://github.com/dasdom/DDHDynamicViewControllerTransitions | 91    |
| https://github.com/RestKit/RestKit                            | 100   |


## Installation

Add this line to your application's Gemfile:

    gem 'readme-score'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install readme-score

## Usage

Pass in a URL:

```ruby
url = "https://raw.githubusercontent.com/AFNetworking/AFNetworking/master/README.md"
score = ReadmeScore.for(url)
score.total_score
# => 95
```

Pass in a Github Repo:

```ruby
score = ReadmeScore.for("afnetworking/afnetworking")
score.total_score
# => 95
```

Pass in HTML:

```ruby
html = "AFNetworking is a delightful networking library for iOS and Mac OS X...."
score = ReadmeScore.for(html)
score.total_score
# => 95
```