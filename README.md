# vue-mdeditor

> A Vue.js project

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

## API
[simplemde-markdown-editor](https://github.com/sparksuite/simplemde-markdown-editor)

#### Toolbar icons

Below are the built-in toolbar icons (only some of which are enabled by default), which can be reorganized however you like. "Name" is the name of the icon, referenced in the JS. "Action" is either a function or a URL to open. "Class" is the class given to the icon. "Tooltip" is the small tooltip that appears via the `title=""` attribute. Note that shortcut hints are added automatically and reflect the specified action if it has a keybind assigned to it (i.e. with the value of `action` set to `bold` and that of `tooltip` set to `Bold`, the final text the user will see would be "Bold (Ctrl-B)").

Additionally, you can add a separator between any icons by adding `"|"` to the toolbar array.

Name | Action | Tooltip<br>Class
:--- | :----- | :--------------
bold | toggleBold | Bold<br>fa fa-bold
italic | toggleItalic | Italic<br>fa fa-italic
strikethrough | toggleStrikethrough | Strikethrough<br>fa fa-strikethrough
heading | toggleHeadingSmaller | Heading<br>fa fa-header
heading-smaller | toggleHeadingSmaller | Smaller Heading<br>fa fa-header
heading-bigger | toggleHeadingBigger | Bigger Heading<br>fa fa-lg fa-header
heading-1 | toggleHeading1 | Big Heading<br>fa fa-header fa-header-x fa-header-1
heading-2 | toggleHeading2 | Medium Heading<br>fa fa-header fa-header-x fa-header-2
heading-3 | toggleHeading3 | Small Heading<br>fa fa-header fa-header-x fa-header-3
code | toggleCodeBlock | Code<br>fa fa-code
quote | toggleBlockquote | Quote<br>fa fa-quote-left
unordered-list | toggleUnorderedList | Generic List<br>fa fa-list-ul
ordered-list | toggleOrderedList | Numbered List<br>fa fa-list-ol
clean-block | cleanBlock | Clean block<br>fa fa-eraser fa-clean-block
link | drawLink | Create Link<br>fa fa-link
image | drawImage | Insert Image<br>fa fa-picture-o
table | drawTable | Insert Table<br>fa fa-table
horizontal-rule | drawHorizontalRule | Insert Horizontal Line<br>fa fa-minus
preview | togglePreview | Toggle Preview<br>fa fa-eye no-disable
side-by-side | toggleSideBySide | Toggle Side by Side<br>fa fa-columns no-disable no-mobile
fullscreen | toggleFullScreen | Toggle Fullscreen<br>fa fa-arrows-alt no-disable no-mobile
guide | [This link](https://simplemde.com/markdown-guide) | Markdown Guide<br>fa fa-question-circle

Customize the toolbar using the `toolbar` option like:

```JavaScript
// Customize only the order of existing buttons
var simplemde = new SimpleMDE({
	toolbar: ["bold", "italic", "heading", "|", "quote"],
});

// Customize all information and/or add your own icons
var simplemde = new SimpleMDE({
	toolbar: [{
			name: "bold",
			action: SimpleMDE.toggleBold,
			className: "fa fa-bold",
			title: "Bold",
		},
		{
			name: "custom",
			action: function customFunction(editor){
				// Add your own code
			},
			className: "fa fa-star",
			title: "Custom Button",
		},
		"|", // Separator
		...
	],
});
```
