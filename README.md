# Viral Nation App Demo

This is a working coded demo of a social media application attempting to meet the user requirements of scenario #2, Jason the up-and-coming influencer.

## Outline

On reading the user/stakeholder requirements I envisioned an app that would provide Jason with daily inspirational content, show him top trends, users, and topics from all main social channels, and offer him an "archive" where he could save chosen items for further review. 

The core functionality revolves around aggregating data from social media platforms in one place using their APIs, while the main working screen is a dashboard rendering the data in different tabs and formats. 

## Inspiration

- Pixlee.com
- Coolors.com
- Pinterest
- Main social outlets

## User flow

The user hits a home/splash screen welcoming them to the app and offers two buttons: a sign up with modal for new users, and get started, which allows users to continue on to use the app without an account (this option would not allow users to save items to their archive). 

The second screen takes the user to a page with the app's 4 main functional areas:    

- **Today**: providing Jason with curated content for daily inspiration. The idea behind this was to offer a small cross section of the day's top trending items from different outlets and in different formats (user accounts, videos, articles). Because Jason doesn't have time to follow social trends, he can have the app show him trending content. The idea could be fleshed out to be either 3-4 items total so as not to overload him, or offer 3-4 items in the above user, video, article categories. 
- **Trends**: takes the user to the app's main dashboard. In it the user is shown a collection of information organized in a few ways. 
- **Learn**: (Not developed) This page would take the user to a section showing articles and video tutorials to help Jason/the user to develop greater skill in content creation.
- **Archive**: (Not developed) The users "cart", the archive is where items a user adds are saved for future inspiration and further exploration.

## Main Dashboard (Trends)

The top tabbed navigation breaks up current social content into 4 areas: Trends, Users, Topics, and provides a Search tab which would allow the user to search the platform randomly.  Each of these tabs shows data from a selected social channel, chosen from the right sidenav popout (the list icon along with the gear icon in the subnav):

*Trends* - returns a list of trending items, top hashtags, articles, topics, etc.  
*Users* - returns a list of top users ranked by followers, likes, shares, stars or whatever that platform uses to prioritize.  
*Topics* - returns an array of articles on the subject of social media, influencers/ing, content creation, etc.  
*Search* - Provides a searchbar to explore the plaform directly. Results would be returned below the search banner.  

Each item/user/article piece of content would offer a number of options for interaction/engagement: a button to add an item to the user's own archive area which stores chosen content like a shopping cart; an option to star or pin or mark as important; a link to visit that item at the source (click to open a new tab in actual Youtube or Instagram), or a ways to explore it more fully via modals which would elaborate and offer further content.

## Functionality

The app operates on collecting and curating data from the various social channels using their APIs. Currently a variety of testing APIs are used as the data source to mock what real data would look like. 

### Original scope

Jason is an up-and-coming influencer.  

He is looking for a platform to find inspirational content easily and save it for later so he can improve his content creation.  

He has a hard time understanding why certain content is getting viral and some don’t.  

He doesn’t have enough time to follow current social media trends.  

Can you solve his problem?