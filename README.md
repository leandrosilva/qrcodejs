# QRCode.js
QRCode.js is javascript library for making QRCode. QRCode.js supports Cross-browser with HTML5 Canvas and table tag in DOM.
QRCode.js has no dependencies.

## Basic Usages
```
<div id="qrcode"></div>
<script type="text/javascript">
new QRCode(document.getElementById("qrcode"), "http://jindo.dev.naver.com/collie");
</script>
```

or with some options

```
<div id="qrcode"></div>
<script type="text/javascript">
var qrcode = new QRCode(document.getElementById("qrcode"), {
	text: "http://jindo.dev.naver.com/collie",
	width: 128,
	height: 128,
	boder: 1,
	colorDark : "#000000",
	colorLight : "#ffffff",
	inputMode: QRCode.InputMode.MODE_ALPHA_NUM,
	correctLevel : QRCode.CorrectLevel.H,
	qualityRatio: 3.125
});
</script>
```
Available options for `inputMode` are

* `QRCode.InputMode.MODE_NUMBER`
* `QRCode.InputMode.MODE_ALPHA_NUM`
* `QRCode.InputMode.MODE_8BIT_BYTE` (default)

For `correctLevel` are

* `QRCode.CorrectLevel.L` for up to 7% damage
* `QRCode.CorrectLevel.M` for up to 15% damage (default)
* `QRCode.CorrectLevel.Q` for up to 25% damage
* `QRCode.CorrectLevel.H` for up to 30% damage

And you might have to play with `qualityRatio` when working with PDF files, e.g. 96 DPI (screen) to 300 DPI (professional printing) is a 3.125 quality ratio. Default is 1.

Additionally, you can use some methods

```
qrcode.clear(); // clear the code.
qrcode.makeCode("http://naver.com"); // make another code.
```

## Browser Compatibility
IE6~10, Chrome, Firefox, Safari, Opera, Mobile Safari, Android, Windows Mobile, ETC.

## License
MIT License

## Contact
twitter @davidshimjs

[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/davidshimjs/qrcodejs/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

