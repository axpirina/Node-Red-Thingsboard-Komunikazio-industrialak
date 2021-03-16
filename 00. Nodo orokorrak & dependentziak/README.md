
# Sarrera

Karpeta honetan Node Red-en beharko dituzuen eta npm idez instalatu ezin dituzuen nodoak aurkituko dituzue.

# Node Red nodo bereziak

<img src="https://github.com/favicon.ico" width="48">


<!-- [START badges] -->

[![Build status](https://github.com/puppeteer/puppeteer/workflows/run-checks/badge.svg)](https://github.com/puppeteer/puppeteer/actions?query=workflow%3Arun-checks) 

<!-- [END badges] -->

<img src="https://i.ibb.co/Jc1yCwM/oteitza-logo.png" height="200" align="right">

###### [Oteitza](http://www.oteitzalp.eus/) | [Hezkuntza](http://www.oteitzalp.eus/eu/hezkuntza) | [Tknika](http://www.oteitzalp.eus/eu/hezkuntza) | [Github](https://github.com/Tknika)

> Errepositorio hau [iombian](https://github.com/Tknika/iombian) eta [IoM2040](https://github.com/Tknika/iom2040) errepositorioen lagungarri aurkezten da, makina industrialetatik ([opc UA](https://opcfoundation.org/about/opc-technologies/opc-ua/), [Modbus](https://modbus.org/), [S7](https://wiki.wireshark.org/S7comm)...) datuak jasotzeko proiektu luze baten barruan. 2017 urtetik industria 4.0 arloan industriaren digitalizazio bidean sortu eta garatzen ari garen erreminten biltegi irekiaren parte dira hurrengo materialak.

<!-- [START usecases] -->

###### Zer egin dezaket?

Hemen aurkituko dituzuen gida gehienak zuen eskola nahiz lantegian aplika ditzakezue. Ezinbesteko elementuak izango dituzue.

- Makinen arteko sare konexioa (Ethernet-Wifi).
- Komunikazio industrialetan erabiltzen diren protokoloren bateko zerbitzaile gisa lan egingo duen makinaren bat(PLC..).
- Gateway bat.
- Pc bat.
- Gogo haundia.
<!-- [END usecases] -->

Emaiguzu txio bat: https://twitter.com/tknika?lang=es

<!-- [START getstarted] -->

<img src="https://github.com/favicon.ico" width="48">

## Hasierako pausuak

### Instalazioa

1. Node Red ireki,  `import`, eta itsatsi.

<img src="https://i.ibb.co/0G03zw7/inportatu.png" width="160" height="160" align="center">

2. Nodoa eskuragarri dugu iada.

<img src="https://i.ibb.co/fNYWVJd/erloju-nodoa.png" width="80"  align="center">


## Nodoak 

Erloju nodoa **DataTimeWidget.json**

```json
[{"id":"b97bc1c0.cb899","type":"ui_template","z":"7583a640.3bbbd8","group":"c982fbb8.1deb38","name":"Clock Toolbar","order":2,"width":"0","height":"0","format":"<script id=\"titleScript\" type=\"text/javascript\">\n\n$(function() {\n    if($('.md-toolbar-tools').length != 0){\n        loadClock();\n    }else setTimeout(loadClock, 500)\n});\n\nfunction loadClock(){\n    $('#clock').remove();\n    var toolbar = $('.md-toolbar-tools');\n    \n    var div = $('<div/>');\n    var p = $('<p/ id=\"clock\">');\n    \n    div.append(p);\n    div[0].style.margin = '5px 5px 5px auto';\n    toolbar.append(div);\n\n    function displayTitle(lh) {\n        p.text(lh); \n    }\n    \n    function upTime() {\n        var d = new Date();\n        p.text(d.toLocaleString());\n    }\n\n    if(document.clockInterval){ \n            clearInterval(document.clockInterval);\n            document.clockInterval = null;\n    }\n        \n    document.clockInterval = setInterval(upTime,1000);\n}\n\n</script>","storeOutMessages":false,"fwdInMessages":false,"templateScope":"global","x":420,"y":80,"wires":[[]]},{"id":"c982fbb8.1deb38","type":"ui_group","z":"","name":"hidden_group","tab":"7c447e96.4b96a","disp":false,"width":"6","collapse":false},{"id":"7c447e96.4b96a","type":"ui_tab","z":"","name":"Zooland Sys","icon":"home","order":1,"disabled":false,"hidden":false}]

```





(c) 2021 [Tknika](https://tknika.eus/) )

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
