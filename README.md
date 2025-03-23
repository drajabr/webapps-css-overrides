# webapps-css-overrides
CSS overrides to make WhatsApp and Telegram WebApps more compact, effectively hiding everything other than chat list and chat box.

## Usage
Extension like [CSS Injector](https://microsoftedge.microsoft.com/addons/detail/css-injector/ennbjebceagmlgmlhhocgccelpggieme) could be used to add these injects as rules to each url.

## Changes for WhatsApp Web
For url: `https://web.whatsapp.com`

```
#app div._aigw {
    max-width: 30%;
}

#app div > header:nth-child(2), /*Sidebar and chat tools*/

#app div > header:nth-child(1), /*Chats header in chat list*/

#pane-side > button, /* Archived chats */


#side > div:nth-child(1), /* Chats search bar */

#side > div:nth-child(2), /* Chats filters */

.xktia5q,  /*Download whatsapp  panel */

#side > div:nth-child(5) /* Download whatsapp pop */
{
    display: none;
}
```

## Changes for Telegram Web
For url: `https://web.telegram.org/k/` *Telegram web version **k** only.*

```
/* Force #column-left to stay at 30% */
#column-left {
    max-width: 30% !important;
    width: 30% !important;
    min-width: 0px !important;
    flex-basis: 30% !important;
    grid-template-columns: 30% auto !important;
    overflow: hidden !important;
}
#column-left .sidebar-header.main-search-sidebar-header, /* Sidebar search */
#chatlist-container .folders-tabs-scrollable, /* Folders/Tabs menu */
#column-center .sidebar-header.topbar.has-avatar /* Chat header */ {
    display: none !important;
}

```
> [!WARNING]
>  I couldn't get telegram web to display split view all the time, I had to zoom out to 80% to get it on 720 width display.
