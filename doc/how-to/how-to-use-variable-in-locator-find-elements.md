---
sidebar_position: 3
sidebar_label: Using Index Variable in Locator to Find A Series Elements
---
# Using Index Variable in Locator to Find A Series Elements
##  Introduction
From Clicknium [Locator](../concepts/locator.md) definition, it supports a parametric locator.   
Users can use the parametric locator in the automation project to replace the ones with the variables or data. It allows the locator to match a series of elements instead of a single target element.

There are two automation cases to demonstrate how to use index variable in the locator to find a series of elements. 

:::tip Notes

For more about the installation and the tutorial of Clicknium Automation, please refer to [here](https://www.clicknium.com/documents).

:::

## Scraping contact list on the slack client

It is an actual user scenario that needs to grab user list information from a slack channel. 

![slack contact list](img/slack_contact_list.png)

After recording one contact item's locator, the user modifies the locator with an index variable.

![slack contact locator](img/slack_locator.png)

Then use loop traversal to locate each contact element and get information.
```python
for i in range(1,13):
    dict = {"index":i}
    if not cc.is_existing(locator.slack.listitem_member, dict):
        continue
    elem_member = ui(locator.slack.listitem_member, dict)
    name = elem_member.get_text()
``` 

### Scraping playlist from Spotify
It is an actual user scenario, which needs to get the playlist information from [spotify](https://open.spotify.com/playlist/6iwz7yurUKaILuykiyeztu).

First, locate "author" and "title" from one item in the playlist.

![spotify playlist](img/spotify_playlist.png)

As the Spotify page is complicated and dynamic, users use "XPath" in the locator.
Modify the locator with the index variable.

![spotify playlist locator1](img/spofity_author_locator.png)

![spotify playlist locator1](img/spofity_title_locator.png)

Then use loop traversal to locate each item in the playlist and get information.
```python
tab = cc.chrome.open("https://open.spotify.com/playlist/6iwz7yurUKaILuykiyeztu")
index = 2

titles = []
artists = []
links = []
while True:
    if not tab.is_existing(locator.chrome.open.div_title, {'index':index}):
        break
    title = tab.find_element(locator.chrome.open.div_title, {'index':index}).get_text()
    artist = []
    link = []
    element = tab.find_element(locator.chrome.open.div_author, {'index':index})
    authers = element.children
    for item in element.children:
        artist.append(item.get_text())
        link.append(item.get_property('href'))

    titles.append(title)
    artists.append(artist)
    links.append(link)
    index += 1
tab.close()
```