Heroku API deployment
gem install travis 
bundle install

You can simply type the command gem install travis$ travis encrypt $(heroku auth:token) --add deploy.api_key.
$ gem install travis$ travis encrypt $(heroku auth:token) --add deploy.api_key

Detected repository as jocontreras/rails_messaging_feb, is this correct? |yes| no
Repository slug (owner/name): |jocontreras/rails_messaging_feb| CraftAcademy/rails_messaging_feb
✔ ~/projects/rails_messaging_feb [develop L|✚ 1]


Go to Heroku Account
Manually copy the API Key and then paste it into command line:
For the ones hosted at travis-ci.com:
travis encrypt pasteAPIKeyHere --add deploy.api_key --pro
For the ones hosted at travis-ci.org:
travis encrypt pasteAPIKeyHere --add deploy.api_key --org
