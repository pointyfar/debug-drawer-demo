## What is this

`hugo-debug-drawer` is a Hugo Theme Component to help debug your Hugo site templates. 

![Debug Drawer](/static/videos/debugdrawer03.gif)


## Where to find

[Theme Component Source](https://github.com/pointyfar/hugo-debug-drawer)

[Demo Source](https://github.com/pointyfar/debug-drawer-demo)

[Demo Site](https://stupefied-hawking-fb6338.netlify.com/)

## How to use

Install as a [theme component](https://gohugo.io/getting-started/quick-start/#step-3-add-a-theme).

Call the `debugdrawer` partial from somewhere in your main theme's layouts.

Optionally, pass configuration object.

```
{{ $options := dict "debugdrawerpanelheight" "500px" "bugcolor" "#000000" "bugbg" "#00C09B" "hidefromdepth" 5 }}

{{ partial "debugdrawer.html" (dict "context" . "options" $options ) }}
```

Add layout information to your template files by including this [`.Scratch`](https://gohugo.io/functions/scratch) variable to your layout files:

```
{{ .Scratch.Set "debugdrawerlayout" "layouts/index.html" }}
```

![Debug Drawer](/static/videos/debugdrawer04.gif)


### Configuration options

`debugdrawerpanelheight`
- Specify the panel's height. Default `300px`.

`bugcolor`
- Specify the foreground color of the bug icon. Default `#FFFFFF`.

`bugbg`
- Specify the background color of the bug icon. Default `#A62639`.

`hidefromdepth` 
- Specify at what depth to hide the elements. Default `5`.

`defaultopen`
- Specify whether the panel is open by default. Default `false`.


## Examples

See [Demo Source](https://github.com/pointyfar/debug-drawer-demo) and 
[Demo Site](https://stupefied-hawking-fb6338.netlify.com/). 

See `hidefromdepth` at work [here](https://stupefied-hawking-fb6338.netlify.com/about/): open `Page` Params panel.


## License

MIT