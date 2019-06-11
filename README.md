# Worldcup Slack Bot

WorldCupBot will notify a Slack channel/group for every matches during a World Cup Game.

**Yes, this works for 2019 Women's World Cup!**

It uses the "unofficial" FIFA json API (the one used for their mobile apps).

It will post a message :
  - when a match starts
  - for every red/yellow card
  - for the half time and end time
  - and of course, for every goal

### Installation

  - Clone this repo
  - Get a incoming webhook URL from Slack:
    - Create an app at https://api.slack.com/apps?new_app=1
    - Go to your app details page at https://api.slack.com
    - Go to "Incoming webhooks" on left navigation
    - and you will find your URL.
    - Now put it into `SLACK_WEBHOOK_URL` in `worldCupNotifier.php`.
  - Make sure you have `php` and `php-curl` installed.
  - Set up a cron to run every minute:

  ````
  * * * * * cd /path/to/folder/worldcup-slack-bot && php worldCupNotifier.php >> worldCupNotifier.log
  ````
