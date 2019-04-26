

### `Step`

```sh
- yarn create react-app my-app
- yarn add git+https://iview_token:XMcNjZRDqXqUiHi2eRFY@gitlab.softbox.com.br/PeD/iview-report.git#feature/remove-pkg-react-md

```

# `Import`
```javascript
 <script src="https://maas.softbox.com.br/iview/loader.js" type="text/javascript"></script>

  <script type="text/javascript">
    magalu.iView.load('2', [], function() {
      console.log('Script Carregado!')
    })
  </script>
```

### `Example`

```javascript

import React, { Component } from 'react';
import Report from  'iview-report/dist/iview-report.min';

import './App.css';

const reportJSON = {
  "filters": [
    {
        "name": "company",
        "label": "Empresa",
        "options": {
            "motorola": "Motorola",
            "samsung": "Samsung",
            "apple": "Apple",
        },
        "value": [
            "motorola",
            "apple",
        ],
    }],
    "widgets": [{ 
      "idRelatorio": "idx",
      "type": "serial",
      "config": {"valueAxes":[{"axisAlpha":0,"position":"left","title":"Visitors from country"}],"startDuration":1,"graphs":[{"balloonText":"<b>[[category]]: [[value]]</b>","fillColorsField":"color","fillAlphas":0.9,"lineAlpha":0.2,"type":"column","valueField":"visits"}],"chartCursor":{"categoryBalloonEnabled":false,"cursorAlpha":0,"zoomable":false},"categoryField":"country","categoryAxis":{"gridPosition":"start","labelRotation":45}},
      "data": [{"country":"USA","visits":3025,"color":"#FF0F00"},{"country":"China","visits":1882,"color":"#FF6600"},{"country":"Japan","visits":1809,"color":"#FF9E01"},{"country":"Germany","visits":1322,"color":"#FCD202"},{"country":"UK","visits":1122,"color":"#F8FF01"},{"country":"France","visits":1114,"color":"#B0DE09"},{"country":"India","visits":984,"color":"#04D215"},{"country":"Spain","visits":711,"color":"#0D8ECF"},{"country":"Netherlands","visits":665,"color":"#0D52D1"},{"country":"Russia","visits":580,"color":"#2A0CD0"},{"country":"South Korea","visits":443,"color":"#8A0CCF"},{"country":"Canada","visits":441,"color":"#CD0D74"}]

  }]

}

class App extends Component {

  render() {
    return <div>
      <div style={{ padding: 16 }}>
        <Report {...reportJSON} />
      </div>
    </div>
  }
}

export default App

```
