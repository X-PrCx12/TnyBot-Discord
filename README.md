[![Build Status](https://travis-ci.org/00firestar00/TnyBot-Discord.svg?branch=master)](https://travis-ci.org/00firestar00/TnyBot-Discord)
[![codecov.io](http://codecov.io/gh/00firestar00/TnyBot-Discord/coverage.svg?branch=master)](https://codecov.io/gh/00firestar00/TnyBot-Discord?branch=master)
[![Discord](https://discordapp.com/api/guilds/809327062116335636/widget.png)](https://discord.gg/bHcdkr5wXg)
[![Instagram](https://instagram.com/ini.pfff/widget.png)]

## TnyBot-Discord
The idea behind TnyBot is that I wanted a Discord bot that had all the functionality of the multiple bots servers were using.

Even though that isn't really practical to have a giant bot with all the commands you could ever think of,
by creating various Cogs (discord.py's version of a plugin system), anyone can mix and match the exact set of commands they want.

I have various example scripts in the root directory.
##### tnybot.py
- This is what I use as a beta bot. All the functionality gets tested here, before I decide to add it to my main bot.

##### heroku.py 
- This is the main public bot. It uses environment variables on Heroku to run and is backed by Postgres (for now)

##### imagebot.py 
- Script I use to fetch images from specified discord channels. 
It downloads all embeds and attachments and organizes them by server/channel. 

- You can add `checksum = True` to the config to avoid duplicate images on disk. This can cause extra downloads though.

##### oauthbot.py
- This is a sample of how to run with a token instead of a user profile.
 
 
If you want to build your own bot, you can add or remove the Cogs from TnyBot as required.
I'll make this more configurable in the future.

#### Config
In order to use the bots, have a look at [sample_config](https://github.com/X-PrCx12/TnyBot-Discord/blob/master/sample_config).

The bots expect the config to be located at `../tnybot_config`.
I didn't want to risk accidentally committing credentials to GitHub, so I put it put it outside this repo. 
This can be quickly edited in the associated py files for now.

##### For Windows Users:
It looks like it will fail to parse the config files unless they are named with an extension. Try renaming the files to `tnybot_config.txt` and fixing the associated bot file to point there.

#### Tests
You can run the tests by using `python3.5 tests.py` or, `python3.5 -m unittest discover tests`.
Or you know, you could just check Travis... Or join my discord, it has Travis webhooks.

#### Heroku
[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/X-PrCx12/TnyBot-Discord)

If you want an easy way to test Tny, without having to install python, postgres, sqlite or anything else he needs,
then use this button. If you don't have an account, you can create one for free. 

`Note: In order to have enough dyno hours for the month, you will need to validate your credit card. 
(Still free as long as you don't go over your limit)`

This will configure everything you need to get it running. Just stick your Bot's token in the field that it asks you to.
If you are having trouble using Heroku, please submit a ticket here, or a pull request if you need something fixed.

