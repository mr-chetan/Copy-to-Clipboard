# Copy to Clipboard


Add this you need to perform action
```html
 <a style="cursor: pointer;" onclick="setClipboard('https://thcb.in')">Copy</a>
```
Add in footer
```html
<script>
    function setClipboard(value) {
        var tempInput = document.createElement("input");
        tempInput.style = "position: absolute; left: -1000px; top: -1000px";
        tempInput.value = value;
        document.body.appendChild(tempInput);
        tempInput.select();
        document.execCommand("copy");
        document.body.removeChild(tempInput);
        if("copy"){
            alert("The text is on the clipboard, try to paste it!");
        }
    }
</script>
```
