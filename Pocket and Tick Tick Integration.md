# Pocket and Tick Tick integration

Being someone who likes to read, I know how important and difficult it's to manage the blogs and articles that I come across daily.

For this purpose, I use a powerful app called `Pocket`. It allows me to keep a track of all the articles that I have read or want to read in the future. (Another equally amazing app is `Instapaper` which does the same job.)

However Pocket, at the time of writing this blog, does not have any widget that allows users to see all articles they have stored.

And I being a "productivity nerd", decided to do something about this.

I like plain simple to-do lists that allow me to track a variety of things such as what movies to watch or what things I need to buy from Amazon during festival sales.

So I decided to club the 2 things close to my heart. The plan was to create a to-do list of all the articles that I save in Pocket.

I initially thought that I can connect the webhook of Pocket with one of my to-do lists. (BTW I use Tick Tick for maintaining my todos.)
However, when I started reading the docs of Pocket, to my surprise they didn't have support webhooks. 😢

So I finally connected the API of the 2 apps and deployed them on a free cloud service to make sure that it runs seamlessly.

Once everything was set up, this is what my productivity looks like.

![](https://raw.githubusercontent.com/akulchhillar/the_quest_of_akul/main/assests/Productivity%20Wall.png)

The todo list in green has all the links that I save in the Pocket app which calls the API of the todo app and creates a new entry with the name and the URL of the article saved.