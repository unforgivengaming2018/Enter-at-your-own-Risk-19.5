# Book Icons

Alternate book icons, so it is clearer when you have read a book.

Inspired by this post on the forums:
[Mod that lets you know you've already read a book?](https://community.7daystodie.com/topic/24306-mod-that-lets-you-know-youve-already-read-a-book/)

## Features

The "already read book" icon is now a check mark,
and it is a semi-translucent green color.

It is also possible to change the "unread book" icon (but not its color).
I did not do this, because in my opinion it made the UI confusing.


## Technical Details

This modlet uses XPath to modify XML files, and does not require SDX or DMT.
It should be compatible with EAC.
It does _not_ contain any new assets (such as images or models).
Servers should automatically push the XML modifications to their clients, so separate client
installation should _not_ be necessary.

Starting a new game should not be necessary, but is always recommended just in case.

### How it works

Open `controls.xml`, and look at this entry in the `item_stack` node:
```xml
<sprite depth="8" name="itemtypeicon" width="24" height="24" sprite="ui_game_symbol_{itemtypeicon}" pos="2,-2" foregroundlayer="true" visible="{hasitemtypeicon}" color="{itemtypeicontint}" />
```

Now, match up the variables (in `{}`) with these properties in the "schematicMaster" item in `items.xml`:
```xml
<property name="ItemTypeIcon" value="book"/>
<property name="AltItemTypeIcon" value="book_read"/>
```

There's a list of `ui_game_symbol_{x}` TGA files in the `XML.txt` file.

Putting it all together, I found the `ui_game_symbol_check.tga` filename,
stripped out the "ui_game_symbol_" prefix,
and used it as the value of the "AltItemTypeIcon" property.

Looking in the code, I also discovered a property with the name "AltItemTypeIconColor".
It can accept an RGB or RGBa color, and this color will be used for the alternate icon tint.
So, I added that property, and used a semi-translucent green color.

### Modifying

You can also change the icon for _unread_ books,
by specifying a new value for the "ItemTypeIcon" value.

However, I tried that, and IMHO it just made the UI confusing.
It was not apparent that you were looking at a schematic, unread or not.

If that is not your opinion, uncomment the relevant code in this modlet's `items.xml` file.
The icon in that code is the "add" image (a plus sign), but you can add any icon you like.

Unfortunately, there does not seem to be any way to change the color of the unread book icon.
