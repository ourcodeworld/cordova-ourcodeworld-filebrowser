# cordova-ourcodeworld-filebrowser Plugin

A cordova implementation of [NoNonsense-FilePicker](https://github.com/spacecowboy/NoNonsense-FilePicker) for Android.

This plugin allow you to select folder and files, and at the same time create folders and create files (not a file is created actually, but it will return the filepath and name of the "choosen path").

<p>
<img src="https://raw.githubusercontent.com/spacecowboy/NoNonsense-FilePicker/master/screenshots/Nexus6-picker-dark.png"
width="25%"
</img>

<img src="https://raw.githubusercontent.com/spacecowboy/NoNonsense-FilePicker/master/screenshots/Nexus10-picker-dark.png"
width="50%"
</img>
</p>

<p>
<img src="https://raw.githubusercontent.com/spacecowboy/NoNonsense-FilePicker/master/screenshots/Nexus6-picker-light.png"
width="25%"
</img>

<img src="https://raw.githubusercontent.com/spacecowboy/NoNonsense-FilePicker/master/screenshots/Nexus10-picker-light.png"
width="50%"
</img>
</p>

## Installation

Install the plugin

```batch
$ cordova plugin add https://github.com/ourcodeworld/cordova-ourcodeworld-filebrowser.git
```

## Usage

A global object `OurCodeWorld.Filebrowser` will be available in your window. This object offers a file picker, folder picker, mixed folder and file picker and the file creation dialog.

```javascript
// Single file selector
window.OurCodeWorld.Filebrowser.filePicker.single({
    success: function(data){
        if(!data.length){
            // No file selected
            return;
        }

        // Array with filepaths
        // ["file:///storage/emulated/0/360/security/file.txt", "file:///storage/emulated/0/360/security/another-file.txt"]
    },
    error: function(err){
        console.log(err);
    }
});

// Single folder selector
window.OurCodeWorld.Filebrowser.folderPicker.single({
    success: function(data){
        if(!data.length){
            // No folders selected
            return;
        }

        // Array with paths
        // ["file:///storage/emulated/0/360/security", "file:///storage/emulated/0/360/security"]
        console.log(data);
    },
    error: function(err){
        console.log(err);
    }
});
```

Check the documentation to see more methods of the plugin like the creation of file, mixed file and folder picker etc.

## External links

- [Documentation](http://ourcodeworld.com/projects/projects-documentation/6/list/cordova-ourcodeworld-filebrowser)
- [Homepage](https://ourcodeworld.github.io/homepages/cordova/cordova-ourcodeworld-filebrowser.html)
