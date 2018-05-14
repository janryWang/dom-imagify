# dom-imagify

> fork from dom-to-image

## Install

```
npm install --save dom-imagify

```

## Usage

```
import {toPng} from "dom-imagify"

const extraStyles = `
@font-face {
    font-family: Roboto;
    src: url(//xxx.xxx.com/roboto-thin.eot);
    font-weight: 200
}
`

toPng(document.body,{
    extraStyles
})
.then(function (dataUrl) {
    var link = document.createElement('a');
    link.download = new Date().getTime()+'.png';
    link.href = dataUrl;
    link.click();
})

```