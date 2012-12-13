Sublime notes
=============

Packages
--------

### AdvancedNewFile

 * `cmd+alt+n` - Specify path and create file
 
### HTTP Requester

 * `Select url`>`cmd+alt+r` - Url is requested

### Emmet
*[Set HTML or related syntax before?]*
 * `[cssSelector] + tab` : Generated HTML 
 

Shortcuts
---------

 * `cmd + ctrl + up/down` - Moves the selected line up/down
 * `cmd + d` - Selects nex occurrence of the selected word *[Editable afterwards]*
 * `cmd + ctrl + g` - Selects all occurrences of the selected word *[Editable afterwards]*

Settings
--------

### Highlight modified tabs

> Add this into [Theme].sublime-theme

    {
        "class": "tab_label",
        "settings": ["highlight_modified_tabs"],
        "parents": [{"class": "tab_control", "attributes": ["dirty"]}],
        "fg": [255, 161, 52]
    }
